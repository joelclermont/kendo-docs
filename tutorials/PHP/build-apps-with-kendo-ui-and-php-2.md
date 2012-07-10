---
title: Intro to Building Apps with Kendo UI And PHP Part 2
slug: tutorial-intro-building-apps-with-kendo-ui-and-php-2
tags: Tutorial
publish: true
---

In Part 1 of this two part tutorial, we went over how to get up
and running with PHP, how to choose and IDE, and how to get some
fake data if you need it.

[Read Part 1](http://docs.kendoui.com/tutorials/PHP/build-apps-with-kendo-ui-and-php)

We built a simple SPA (single page application) which displays a list of sales
employees and each employee can be expanded to show the territories they are
responsible for.  In this tutorial, we are going to extend that application to allow a
user to create, update and delete data.

### Business Requirements

The requirements are as follows:

**Requirement 1:** Users should be able to update an employee’s last name, but
not their first name.  This is because first names don’t change, but last
names sometimes do.

- Last name cannot be null
- Add save and cancel buttons

**Requirement 2:** Users should be able to add new territories to a sales
employee.

Not terribly complex requirements to implement, but this will allow us to work
through how we can use the **DataSource** and **models** along with editable
grids.

### Requirement 1: Update The Last Name

The first thing that we should do is tell the grid of employees that it is
editable.  This is done by setting **editable: true.**


	$("#grid").kendoGrid({
        dataSource: {
            transport: {
                read: "data/employees.php"
            },
            schema: {
                data: "data"
            }
        },
        columns: [{ field: "FirstName" }, { field: "LastName" }],
        detailTemplate: kendo.template($("#template").html()),
        detailInit: detailInit,
        editable: true
    });


Setting **editable: true** is not enough to make the grid editable because the
grid doesn’t have nearly enough information to know how to handle the editing
process.  We want the last name to be editable but not the first.
Additionally, we don’t want people to be able to null out the last name.

The grid will get this information from the DataSource, but we need to define
the “model” property of the schema which will tell the DataSource the exact
structure of the data, as well as allowing us to specify validation rules for
the data.


    $("#grid").kendoGrid({
        dataSource: {
            transport: {
                read: "data/employees.php"
            },
            schema: {
                data: "data",
                model: {
                    id: "EmployeeID",
                    fields: {
                        FirstName: { editable: false },
                        LastName: { validation: { required: true} }
                    }
                }
            }
        },
        columns: [{ field: "FirstName" }, { field: "LastName" }],
        detailTemplate: kendo.template($("#template").html()),
        detailInit: detailInit,
        editable: true
    });


The above **schema** property has been modified.  It now contains a **model**
object.  That model defines the primary key for the employee data, which is of
course the EmployeeID.  This is the field that helps the model know how to
distinguish unique objects.  The **fields **property designates the rest of
the fields in the data source that we are using.  In our case, it’s the first
and last name.  Each **field** property has some additional information with
it.

**FirstName:** We decided first names don’t change so we don’t want people
editing this field.  This is accomplished by setting **editable: false **for
the FirstName.

**LastName:** This field is editable, but we don’t want users blanking it out,
so we can make it required by setting the **validation** object.

The grid now has enough information to make the grid editable.  If you run the
project, you will notice that you can click on the Last Name and it will
become and editable textbox.  However, if you click on the First Name, nothing
happens because you can’t edit it.  Go ahead and try to blank out the Last
Name and press enter.  You get a validation message.

![Validation Message](https://github.com/telerik/kendo-docs/raw/master/tutorials/images/Part-_7E9D-9_2.png)

For more information on all the things you can do with
validation rules, make sure you check out the Kendo UI Validation Demos.

Before we can go any further with this, we need to create an endpoint for
updating the last name.

**Update Endpoint**

So far, we have all our endpoints in a data folder.  Each endpoint is named
for the table which it theoretically represents in the database.  We could do
this one of two ways.

1. We could create subfolders for the endpoints and then have read, create,
update and delete methods in each one.

2. Listen for the HTTP verb type and respond appropriately.

Number 2 is more RESTful than 1, so we will implement it that way. REST is wonderful and you should
learn much more about it, but there isn’t space to fully cover that and the
current topic in this tutorial.

What is meant by the HTTP verb is that if the request is a GET, we will treat it
as a read.  If it is a POST, we treat it as an update.  Additionally, if we
were doing create or delete we would use the PUT for create and the DELETE for
delete.

Inside the **employees.php** file in the **data** folder, we need to write
scenarios for the different request types.  I did this by determining what the
verb was using the $.SERVER[“REQUEST_TYPE”] method and responding
appropriately.

	<?php
	
		$link = mysql_pconnect("localhost", "root", "root") or die("Unable To Connect To Database Server");

		mysql_select_db("northwind") or die("Unable To Connect To Northwind");

		// add the header line to specify that the content type is JSON
		header("Content-type: application/json");

		// determine the request type
		$verb = $_SERVER["REQUEST_METHOD"];

		// handle a GET 
		if ($verb == "GET") {
			$arr = array();

			$rs = mysql_query("SELECT EmployeeID, LastName, FirstName FROM Employees");

			while($obj = mysql_fetch_object($rs)) {

				$arr[] = $obj;

			}
			echo "{\"data\":" .json_encode($arr). "}";
		}

		// handle a POST  
		if ($verb == "POST") {

			// DISCLAIMER: It is better to use PHP prepared statements to communicate with the database. 
			//             this provides better protection against SQL injection.
			//             [http://php.net/manual/en/pdo.prepared-statements.php][4]
			// get the parameters from the post. escape them to protect against sql injection.

	        $lastName = mysql_real_escape_string($_POST["LastName"]);
	        $employeeId = mysql_real_escape_string($_POST["EmployeeID"]);

	        $rs = mysql_query("UPDATE Employees SET LastName = '" .$lastName ."' WHERE EmployeeID = " .$employeeId);

	        echo json_encode($rs);
	    }

    ?>

**A Few Things Of Note**

The **header** call was moved to the top because we need it no matter what.  The
next thing we did was determine the verb and set the **$verb** variable.  The
first **if** handles the GET or the read, and the second handles the POST or
update.

In the POST method, we pulled the **LastName** value and **EmployeeID** off the
request, since the Kendo UI DataSource sent them as parameters.  It’s then
just a matter of executing a simple update statement.  When doing a CRUD
operation like this, the **mysql_query** will return a simple **true** if the
statement executed and a **false** if it did not.  The only thing the
DataSource is looking for is a 200 from the server, so it really doesn’t
matter what you return, as long as it’s JSON.

**Add The Endpoint To The DataSource**

The DataSource needs to know about the update endpoint and that we want a
POST.  This is done by specifying the **update** object on the **transport**.

The other changes that were made to the grid were to make it navigable, which enables
us to exit the cell be edited by using the “enter” key, and also add “Save”
and “Cancel” buttons in the toolbar.  All of this is trivial with the grid.
The grid code now looks like this.


    $("#grid").kendoGrid({
        dataSource: {
            transport: {
                read: "data/employees.php",
                update: {
                    url: "data/employees.php",
                    type: "POST"
                }
            },
            schema: {
                data: "data",
                model: {
                    id: "EmployeeID",
                    fields: {
                        FirstName: { editable: false },
                        LastName: { validation: { required: true} }
                    }
                }
            }
        },
        columns: [{ field: "FirstName" }, { field: "LastName" }],
        detailTemplate: kendo.template($("#template").html()),
        detailInit: detailInit,
        editable: true,
        navigable: true,  // enables keyboard navigation in the grid
        toolbar: [ "save", "cancel" ]  // adds save and cancel buttons
    });


### Failed Request

PHP is going to return a 200, even if the SQL statement doesn’t execute.  We
don’t want this.  Then the grid thinks the data update happened, but in
reality, it failed.  The UI is now out of sync with the database.

We need for PHP to return a server error.  To do this, we just need to add the
header.  Our POST function now looks like this…


    // handle a POST
    if ($verb == "POST") {

    	// DISCLAIMER: It is better to use PHP prepared statements to communicate with the database.
        //             this provides better protection against SQL injection.
        //             [http://php.net/manual/en/pdo.prepared-statements.php][4]

		// get the parameters from the post. escape them to protect against sql injection.

        $lastName = mysql_real_escape_string($_POST["LastName"]);
        $employeeId = mysql_real_escape_string($_POST["EmployeeID"]);

        $rs = mysql_query("UPDATE Employees SET LastName = '" .$lastName ."' WHERE EmployeeID = " .$employeeId);

        if ($rs) {
            echo json_encode($rs);
        }
        else {
            header("HTTP/1.1 500 Internal Server Error");
            echo "Update failed for EmployeeID: " .$employeeId;
        }
    }



If the update succeeds, a “true” is returned.  If the update fails, a 500
server error is returned and the grid will not reflect that the update has
been made.  If you want to provide additional information on the error, you
can listen to the **error** event on the DataSource **update** method.


    $("#grid").kendoGrid({
        dataSource: {
            transport: {
                read: "data/employees.php",
                update: {
                    url: "data/employee.php",
                    type: "POST"
                }
            },
            error: function(e) {
                alert(e.responseText);
            }
            schema: {
                data: "data",
                model: {
                    id: "EmployeeID",
                    fields: {
                        FirstName: { editable: false },
                        LastName: { validation: { required: true} }
                    }
                }
            }
        },
        columns: [{ field: "FirstName" }, { field: "LastName" }],
        detailTemplate: kendo.template($("#template").html()),
        detailInit: detailInit,
        editable: true,
        navigable: true,  // enables keyboard navigation in the grid
        toolbar: [ "save", "cancel" ]  // adds save and cancel buttons
    });



#### Sample Failure…

![Sample Failure](https://github.com/telerik/kendo-docs/raw/master/tutorials/images/Part-_7E9D-10_2.png)

### Requirement 2: Add Sales Territories

In order to enable our users to add sales territories, we need to give the
details grid a model as well and specify it’s structure.  We also need to
specify the endpoint for a create.  In our RESTful style, we will use a “PUT”
HTTP verb as the type and specify the **create** method of the **transport**.
We also moved the DataSource out of the grid declaration and into a variable
that we can access later.

In JavaScript, if you don’t put **var **in front of your variable, it becomes
a global variable.  This is generally considered bad practice, but in the name
of simple demonstration, it is being done here.


    employeeTerritoriesDS = new kendo.data.DataSource({
        transport: {
            read: "data/territories.php",
            create: {
                url: "data/employeeTerritories.php",
                type: "PUT"
            },
        },
        schema: {
            data: "data",
            model: {
                id: TerritoryID,
            }
        },
        serverFiltering: true,
        filter: { field: "EmployeeID", operator: "eq", value: e.data.EmployeeID }
    });


    // create a subgrid for the current detail row, getting territory data for this employee
    detailRow.find(".subgrid").kendoGrid({
        dataSource: employeeTerritoriesDS,
        columns: [{ title: "Territories", field: "TerritoryDescription" }],
        toolbar: [ "save" ]
    });


We also added a **save** button on the toolbar like we did in the parent grid.

At this point, we need to add a way for users to add a new territory to a
user.  There is a catch here though.  We can’t just let them enter free text.
We have a table of Territories and a table of Employees and they are related
via a Lookup Table called **EmployeeTerritories**.  If we let the user enter
free text, we then have to create the territory, get it’s newly created ID and
update the **EmployeeTerritories** table.  Beyond that, the user could enter a
value that is already in the **Territories** table.  That defeats the purpose
of our lookup.  What we really need, is a list of choices.

#### Enter The ComboBox

It was mentioned earlier that our details template was simple, but
we could expand on it?  We’re going to do that now.  Our new template will
contain an input which we can turn into a ComboBox and a button on which we
can handle the click and add the item to the grid.


    <script type="text/x-kendo-template" id="template">
        <div>
            <div style="margin-bottom: 10px;">
                <input id="territory_#= data.EmployeeID #" class="comboBox" />
                <button class="k-button add-territory" data-employee-id="#= data.EmployeeID #"
                               onclick="addTerritory(this)" >Add</button>
            </div>
            <div class="subgrid"></div>
        </div>
    </script>

So we added an input and a button.  But what is this funky #= syntax?

This is a Kendo UI Template syntax. It’s going to replace **data.EmployeeID**
with the actual **EmployeeID**.  The **e** argument that goes into the
**detailInit(e)** function also gets passed to our template.  **EmployeeID** is found on the **data** object off the **e** parameter.  We are dynamically
composing an ID that will help us grab that ComboBox later much easier.  We
are also adding the **EmployeeID** as a data attribute on the button so we can
get the **EmployeeID **back much easier and thusly get the instance of the
ComboBox much easier.  I also added an **onlick** event to the button and
passed in the button itself as a parameter.  This **addTerritory** event is
where we will actually add the item to the grid.

On the **detailInit()** we need to define a DataSource for our ComboBox and
create the widget.  We are going to need an additional file in the **data** folder.  At this point, it makes more sense for our current
**territories.php** file to be renamed to **employeeTerritories.php** because
that’s really what it represents.  I renamed that and updated the DataSource
instance with the right endpoints on the **transport**.

Now create a new php file in **data,** and call it **territories.php**.  This
file will get us a list of Territories our users can pick from.  But we don’t
want the user assigning duplicate territories so we need to filter those out.
We will select everything that is not currently assigned to them.  You will
notice below in the transport that I add the **EmployeeID **on to the end of
the **read** so it gets passed as a query string variable.


    // create the datasource
    territoriesDS = new kendo.data.DataSource({
        transport: {
            read: "data/territories.php?EmployeeID=" + e.data.EmployeeID
        },
        schema: {
            data: "data",
            model: {
                id: "TerritoryID"
            }
        }

    });


And the **territories.php** endpoint:


    <?php

	    $link = mysql_pconnect("localhost", "root", "root") or die("Could not connect");

	    mysql_select_db("northwind") or die("Could not select database");

	    $arr = array();

	    // DISCLAIMER: It is better to use PHP prepared statements to communicate with the database.
	    //             this provides better protection against SQL injection.
	    //             [http://php.net/manual/en/pdo.prepared-statements.php][4]

	    // get the parameters from the get. escape them to protect against sql injection.
	    $employeeId = mysql_real_escape_string($_REQUEST["EmployeeID"]);

	    $rs = mysql_query("SELECT t.TerritoryID, TRIM(t.TerritoryDescription) AS TerritoryDescription
	                       FROM EmployeeTerritories et
	                       INNER JOIN Territories t ON et.TerritoryID = t.TerritoryID
	                       WHERE et.EmployeeID != " .$employeeId
	                       . " ORDER BY t.TerritoryDescription ASC");

	    while($obj = mysql_fetch_object($rs)) {

	        $arr[] = $obj;

	    }


	    header("Content-type: application/json");

	    echo "{\"data\":" .json_encode($arr). "}";

    ?>


The DataSource and endpoint are all configured so we are set to turn this
input from the template into a ComboBox.  To do this,.we select the item and
call **kendoComboBox()**, passing in the DataSource and defining what the text
and value fields are.


    // create the autocomplete
    detailRow.find(".comboBox").kendoComboBox({
        dataSource: territoriesDS,
        dataTextField: "TerritoryDescription",
        dataValueField: "TerritoryID"
    });

Now if you view the page, we have a nifty drop down you can either type in, or
select from.  Oh, and we also switched the theme to **default** just for fun!

![Nifty Drop Down](https://github.com/telerik/kendo-docs/raw/master/tutorials/images/Part-_7E9D-11_4.png)

Now we have a ComboBox that returns only the territories that
are not currently assigned to this person.  Now let’s add the event for
handling the button click.


    var addTerritory = function(sender) {

        // get the employee id off the data-employee-id attribute of the button
        var employeeId = $(sender).data("employee-id");

        // get a reference to the combobox which contains the selected item
        var comboBox = $("#territory_" + employeeId).data("kendoComboBox");

        // add the item to the datasource - it is thusly added to the grid
        employeeTerritoriesDS.add({ EmployeeID: employeeId, TerritoryDescription: comboBox.text(),  TerritoryID: comboBox.value() });

        // remove the current item from the combobox - it's no longer a valid selection
        territoriesDS.remove(comboBox.value());

        // clear the text of the combobox
        comboBox.text("");
    }

The first line gets the **EmployeeID** off the data attribute on the button.

The second line gets the ComboBox by building the dynamic ID and getting a
reference to an instance of the ComboBox.

**_Kendo UI Widgets are always referenced by data(“kendoWidgetName”) after
initialization._**

The third line actually adds an item to the **employeeTerritoriesDS**.  This
is the power of the DataSource.  We aren’t going to interact with the remote
data, only the local model.  The DataSource will take care of sending it to
the database after we click the save button.

The last two lines remove the item we just added from the ComboBox, because it
is no longer available and then clear the text of the ComboBox box.

#### No DELETE or PUT in PHP

Let’s add the **PUT** method to the **employeeTerritories.php** file.  Unlike
the GET and POST, PHP does not contain a global container for PUT or DELETE.

In any case, we can read in the input, assign it to an array and then access
the variables we send over the wire as part of the form values.


    if ($verb == "PUT") {
        $request_vars = Array();
        parse_str(file_get_contents('php://input'), $request_vars );

		// DISCLAIMER: It is better to use PHP prepared statements to communicate with the database.
		//             this provides better protection against SQL injection.
		//             [http://php.net/manual/en/pdo.prepared-statements.php][4]
		
        // get the parameters from the get. escape them to protect against sql injection.

        $territoryId = mysql_real_escape_string($request_vars["TerritoryID"]);

        $employeeID = mysql_real_escape_string($request_vars["EmployeeID"]);

        $sql = "INSERT INTO EmployeeTerritories (EmployeeID, TerritoryID) VALUES (" .$employeeID ."," .$territoryId .")";

        $rs = mysql_query($sql);

        if ($rs) {
            echo true;
        }
        else {
            header("HTTP/1.1 500 Internal Server Error");
            echo false;
        }
    }

Now run the application and you can add new items to the grid.  Once you click
the **Save** button in the grid toolbar, the inserts will be sent to the
server.  However, **TerritoryID** will be empty.  Why is this?  This is
actually because we didn’t assign a **TerritoryID** when we added the model
object to the DataSource on the subgrid.  The **TerritoryID** is currently the
primary key.  The DataSource will not recognize the object as being a newly
created object if you assign a value to it’s primary key and thusly nothing
will get sent to the server on create.

The real issue here is that the primary key for the subgrid is really a
compound key.  It’s the **EmployeeID** and the **TerritoryID** together which
define a unique record.  Let’s go back and do some trickery in the SQL to make
that appear to be the case.  We can concatenate the **EmployeeID **and
**TerritoryID** to make our own compound key.


	$rs = mysql_query("SELECT CONCAT(et.EmployeeID, et.TerritoryID) AS EmployeeTerritoryID, t.TerritoryID, e.EmployeeID,
                       TRIM(t.TerritoryDescription) AS TerritoryDescription
                       FROM Territories t
                       INNER JOIN EmployeeTerritories et ON t.TerritoryID = et.TerritoryID
                       INNER JOIN Employees e ON et.EmployeeID = e.EmployeeID
                       WHERE e.EmployeeID = " .$employeeID);


And the model for the DataSource now becomes:

    model: {
        id: "EmployeeTerritoryID"
    }


No need to add the **EmployeeID** or **TerritoryID** to the model definition.
It’s smart enough to pick those up on its own!

It is highly recommended that you use some sort of MVC framework with your PHP.
[Zend](http://www.zend.com/en/) is popular and [CodeIgniter](http://codeigniter.com/) looks promising. It really takes some of the headache out of the manual things
that we did here.

   [4]: http://php.net/manual/en/pdo.prepared-statements.php(http://php.net/manual/en/pdo.prepared-statements.php)


