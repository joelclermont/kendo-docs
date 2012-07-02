---
title: Overview
publish: true
---

### DropDownList

The DropDownList HtmlHelper extension is a server-side wrapper for the [Kendo UI DropDownList](http://www.kendoui.com/documentation/ui-widgets/dropdownlist/overview.aspx) widget.

### Getting Started

There are two ways to bind a Kendo DropDownList for ASP.NET MVC:

*   **server** - the data will be serialized to the client. No Ajax requests will be made.
*   **ajax** - the dropdownlist will make ajax request to get the data. 

#### Configure the Kendo DropDownList for server binding

Here is how to configure the Kendo DropDownList  for server binding to the Northwind Products table using Linq to SQL:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method and pass the Products table as the model:

    public ActionResult Index()
    {
    NorthwindDataContext northwind = new NorthwindDataContext();
    
    return View(northwind.Products);
    }
        3.  Make your view strongly typed:

#### WebForms
 
    <%@ Page Language="C#" MasterPageFile="~/Views/Shared/Site.Master" 
       Inherits="System.Web.Mvc.ViewPage<IEnumerable<MvcApplication1.Models.Product>>" %>
              
#### Razor
 
    @model IEnumerable<MvcApplication1.Models.Product>
             4.  Add a server bound dropdownlist:

#### WebForms
 
    <%: Html.Kendo().DropDownList()
        .Name("productDropDownList") //The name of the dropdownlist is mandatory. It specifies the "id" attribute of the widget.
        .DataTextField("ProductName") //Specifies which property of the Product to be used by the dropdownlist as a text.
        .DataValueField("ProductID") //Specifies which property of the Product to be used by the dropdownlist as a value.
        .BindTo(Model)   //Pass the list of Products to the dropdownlist.
        .SelectedIndex(10) //Select an item with index 10\. Note that the indexes are zero based.
    %>
              
#### Razor
 
    <pre class="prettyprint">@(Html.Kendo().DropDownList()
      .Name("productDropDownList") //The name of the dropdownlist is mandatory. It specifies the "id" attribute of the widget.
      .DataTextField("ProductName") //Specifies which property of the Product to be used by the dropdownlist as a text.
      .DataValueField("ProductID") //Specifies which property of the Product to be used by the dropdownlist as a value.
      .BindTo(Model)   //Pass the list of Products to the dropdownlist.
      .SelectedIndex(10) //Select an item with index 10\. Note that the indexes are zero based.
    ) </pre>  

#### Configure the Kendo DropDownList for ajax binding

Here is how to configure the Kendo DropDownList for ajax binding to the Northwind Products table using Linq to SQL:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create an action method which renders the view:

    public ActionResult Index()
    {
    return View();
    }
        3.  Create a new action method and pass the Products table as Json result:

    public JsonResult GetProducts()
    {
    NorthwindDataContext northwind = new NorthwindDataContext();
    
    return Json(northwind.Products);
    }
        4.  Add a ajax bound dropdownlist:

#### WebForms
 
    <%: Html.Kendo().DropDownList()
        .Name("productDropDownList") //The name of the dropdownlist is mandatory. It specifies the "id" attribute of the widget.
        .DataTextField("ProductName") //Specifies which property of the Product to be used by the dropdownlist as a text.
        .DataValueField("ProductID") //Specifies which property of the Product to be used by the dropdownlist as a value.
        .DataSource(source => 
        {
                source.Read(read =>
               {
                        read.Action("GetProducts", "Home") //Set the Action and Controller name
                            .ServerFiltering(true); //If true the DataSource will not filter the data on the client.
               });
        })
        .SelectedIndex(0) //Select first item.
    %>
              
#### Razor
 
    <pre class="prettyprint">@(Html.Kendo().DropDownList()
        .Name("productDropDownList") //The name of the dropdownlist is mandatory. It specifies the "id" attribute of the widget.
        .DataTextField("ProductName") //Specifies which property of the Product to be used by the dropdownlist as a text.
        .DataValueField("ProductID") //Specifies which property of the Product to be used by the dropdownlist as a value.
        .DataSource(source => 
        {
                source.Read(read =>
               {
                        read.Action("GetProducts", "Home") //Set the Action and Controller name
                            .ServerFiltering(true); //If true the DataSource will not filter the data on the client.
               });
        })
        .SelectedIndex(0) //Select first item.
    ) </pre>  

### Accessing an Existing DropDownList

You can reference an existing DropDownList instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/dropdownlist/methods.aspx) to control its behavior.

  

#### Accessing an existing DropDownList instance
 
    //Put this after your Kendo DropDownList for ASP.NET MVC declaration
    <script>
    $(function() { 
    // Notice that the Name() of the dropdownlist is used to get its client-side instance
    var grid = $("#productDropDownList").data("kendoDropDownList");
    });
    </script>
      

### Handling Kendo UI DropDownList events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/dropdownlist/events.aspx) exposed by Kendo UI DropDownList:

  

#### WebForms - subscribe by handler name
 
    <%: Html.Kendo().DropDownList()
        .Name("dropdownlist")
        .BindTo(new string[] { "Item1", "Item2", "Item3" })
        .Events(e => e
            .Select("dropdownlist_select")
            .Change("dropdownlist_change")
        )
    %>
    <script>
    function dropdownlist_select() {
        //Handle the select event
    }
    
    function dropdownlist_change() {
        //Handle the change event
    }
    </script>
       

#### Razor - subscribe by handler name
 
    @(Html.Kendo().DropDownList()
      .Name("dropdownlist")
      .BindTo(new string[] { "Item1", "Item2", "Item3" })
      .Events(e => e
            .Select("dropdownlist_select")
            .Change("dropdownlist_change")
      )
    )
    <script>
    function dropdownlist_select() {
        //Handle the select event
    }
    
    function dropdownlist_change() {
        //Handle the change event
    }
    </script>
       

#### Razor - subscribe by template delegate
 
    @(Html.Kendo().DropDownList()
      .Name("dropdownlist")
      .BindTo(new string[] { "Item1", "Item2", "Item3" })
      .Events(e => e
          .Select(@<text>
            function() {
                //Handle the select event inline
            }
          </text>)
          .Change(@<text>
            function() {
                //Handle the change event inline
            }
            </text>)
      )
    )
     