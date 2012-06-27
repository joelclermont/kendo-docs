---
title: kendo.data.DataSource
tags: api,framework
publish: true
---

# kendo.data.DataSource

## Description



The DataSource component is an abstraction for using local (arrays of JavaScript objects) or
remote (XML, JSON, JSONP) data. It fully supports CRUD (Create, Read, Update, Destroy) data
operations and provides both local and server-side support for Sorting, Paging, Filtering, Grouping, and Aggregates.


### Getting Started

#### Creating a DataSource bound to local data

    var movies = [ {
          title: "Star Wars: A New Hope",
          year: 1977
       }, {
         title: "Star Wars: The Empire Strikes Back",
         year: 1980
       }, {
         title: "Star Wars: Return of the Jedi",
         year: 1983
       }
    ];
    var localDataSource = new kendo.data.DataSource({data: movies});

#### Creating a DataSource bound to a remote data service (Twitter)

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: {
                // the remote service url
                url: "http://search.twitter.com/search.json",
    
                // JSONP is required for cross-domain AJAX
                dataType: "jsonp",
    
                // additional parameters sent to the remote service
                data: {
                    q: "html5"
                }
            }
        },
        // describe the result format
        schema: {
            // the data which the data source will be bound to is in the "results" field
            data: "results"
        }
    });

### Binding UI widgets to DataSource


Many Kendo UI widgets support data binding, and the Kendo UI DataSource is an ideal
binding source for both local and remote data. A DataSource can be created in-line
with other UI widget configuration settings, or a shared DataSource can be created
to enable multiple UI widgets to bind to the same, observable data collection.

#### Creating a local DataSource in-line with UI widget configuration

    $("#chart").kendoChart({
        title: {
            text: "Employee Sales"
        },
        dataSource: new kendo.data.DataSource({
            data: [
            {
                employee: "Joe Smith",
                sales: 2000
            },
            {
                employee: "Jane Smith",
                sales: 2250
            },
            {
                employee: "Will Roberts",
                sales: 1550
            }]
        }),
        series: [{
            type: "line",
            field: "sales",
            name: "Sales in Units"
        }],
        categoryAxis: {
            field: "employee"
        }
    });

#### Creating and binding to a sharable remote DataSource

    var sharableDataSource = new kendo.data.DataSource({
        transport: {
            read: {
                url: "data-service.json",
                dataType: "json"
            }
        }
    });
    
    // Bind two UI widgets to same DataSource
    $("#chart").kendoChart({
        title: {
            text: "Employee Sales"
        },
        dataSource: sharableDataSource,
        series: [{
            field: "sales",
            name: "Sales in Units"
        }],
        categoryAxis: {
            field: "employee"
        }
    });
    
    $("#grid").kendoGrid({
        dataSource: sharableDataSource,
            columns: [
            {
                field: "employee",
                title: "Employee"
            },
            {
                field: "sales",
                title: "Sales",
                template: '#= kendo.toString(sales, "N0") #'
        }]
    });

## Configuration

### aggregate `Array | Object`*(default: undefined)*

 Sets fields on which initial aggregates should be calculated

#### Example

    // calculates total sum of unitPrice field's values.
    [{ field: "unitPrice", aggregate: "sum" }]

### data `Array`

Specifies the local JavaScript object to use for the data source.

#### Example

    // bind the datasource to a local JavaScript array
    var orders = [ { orderId: 10248, customerName: "Paul Smith" }, { orderId: 10249, customerName: "Jane Jones" }];
    var dataSource = new kendo.data.DataSource({
         data: orders
    });

### filter `Array | Object`*(default: undefined)*

 Sets initial filter

#### Example

    // returns only data where orderId is equal to 10248
    filter: { field: "orderId", operator: "eq", value: 10248 }
    
    // returns only data where orderId is equal to 10248 and customerName starts with Paul
    filter: [ { field: "orderId", operator: "eq", value: 10248 },
              { field: "customerName", operator: "startswith", value: "Paul" } ]

### group `Array | Object`*(default: undefined)*

 Sets initial grouping

#### Example

    // groups data by orderId field
    group: { field: "orderId" }
    
    // groups data by orderId and customerName fields
    group: [ { field: "orderId", dir: "desc" }, { field: "customerName", dir: "asc" } ]

### page `Number`*(default: undefined)*

 Sets the index of the displayed page of data.

#### Example

    var dataSource = new kendo.data.DataSource({
        page: 2 // displays the second page of data in the bound widget
    });

### pageSize `Number`*(default: undefined)*

 Sets the number of records which contains a given page of data.

#### Example

    var dataSource = new kendo.data.DataSource({
        pageSize: 5 // 5 records per page of data
    });

### schema `Object`

Set the object responsible for describing the raw data format

#### Example

    var dataSource = new kendo.data.DataSource({
         transport: {
           read: "Catalog/Titles",
         },
         schema: {
             aggregates: function(data) {
                  // returns aggregates
             },
             data: function(data) {
                 return data.result;
             },
             total: function(data) {
                 return data.totalCount;
             },
             parse: function(data) {
                 return data;
             },
             type: "jsonp"
         }
     });

### schema.aggregates `Function`

Returns the calculated aggregates as object.
Result should have the following format:

#### Example

    {
      FIEL1DNAME: {
          FUNCTON1NAME: FUNCTION1VALUE,
          FUNCTON2NAME: FUNCTION2VALUE
      },
      FIELD2NAME: {
          FUNCTON1NAME: FUNCTION1VALUE
      }
    }

#### Example

    {
      unitPrice: {
          max: 100,
          min: 1
      },
      productName: {
          count: 42
      }
    }

### schema.data `Function`

Returns the deserialized data as array.

### schema.groups `Function`

Used instead of data function if remote grouping operation is executed.
 Returns the deserialized data as array.
Result should have the following format:

#### Example

    [{
      aggregates: {
          FIEL1DNAME: {
              FUNCTON1NAME: FUNCTION1VALUE,
              FUNCTON2NAME: FUNCTION2VALUE
          },
          FIELD2NAME: {
              FUNCTON1NAME: FUNCTION1VALUE
          }
      },
      field: FIELDNAME, // the field name on which is grouped
      hasSubgroups: true, // false if there are not sub group items and this is the top most group
      items: [
      // either the inner group items (if hasSubgroups is true) or the data records
         {
             aggregates: {
                 //nested group aggregates
             },
             field: NESTEDGROUPFIELDNAME,
             hasSubgroups: false,
             items: [
             // data records
             ],
             value: NESTEDGROUPVALUE
         },
         //nestedgroup2, nestedgroup3, etc.
      ],
      value: VALUE // value of the field on which is grouped
    }
    // group2, group3, etc.
    ]

### schema.model `Object`

Describes the Model

#### Example

    var dataSource = new kendo.data.DataSource({
           //..
            schema: {
                model: {
                    id: "ProductID",
                    fields: {
                         ProductID: {
                            //this field will not be editable (default value is true)
                            editable: false,
                            // a defaultValue will not be assigned (default value is false)
                            nullable: true
                         },
                         ProductName: {
                             validation: { //set validation rules
                                 required: true
                             }
                         },
                         UnitPrice: {
                           //data type of the field {Number|String|Boolean|Date} default is String
                           type: "number",
                           // used when new model is created
                           defaultValue: 42,
                           validation: {
                               required: true,
                               min: 1
                           }
                       }
                   }
               }
           }
       })

### schema.model.fields `Object`

Describes the model fields and their properties


Available field attrbiutes:



##### *editable*

Determines if this field will be editable (default value is true)

##### *defaultValue*

The value which will be used to populate the field when new non-existing model is created.
            Default value is type attrbiute specific i.e. string fields will have empty string as defaultValue

##### *nullable*

Determines if the value set through defaultValue will be used (default value is false)

##### *type*

The type of the field {Number|String|Boolean|Date}. Default type is string.

##### *validation*

A set of validation rules. The built-in KendoUI Validator rules are available as well as custom rules.

#### Example

    var dataSource = new kendo.data.DataSource({
           //..
            schema: {
                model: {
                    fields: {
                         UnitPrice: {
                           validation: {
                               required: true,
                               min: 1,
                               date: { message: "My custom message" }, // custom message
                               aCustomRule: function(input) { // custom validation rule
                                  return input.val() === "foo"
                               }
                           }
                       }
                   }
               }
           }
       })

### schema.model.id `Number | String`

The field use to identify an unique Model instance

### schema.parse `Function`

Executed before deserialized data is read.
 Appropriate for preprocessing of the raw data.

### schema.total `Function`

Returns the total number of records.

### schema.type `String`

Specify the type of schema { xml | json }

### serverAggregates `Boolean`*(default: false)*

 Determines if aggregates should be calculated on the server.

#### Example

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: "orders.json"
        },
        serverAggregates: true,
        aggregate: { field: "orderId", operator: "eq", value: 10248 } // return only data where orderId equals 10248
    });

### serverFiltering `Boolean`*(default: false)*

 Determines if filtering of the data should be handled on the server.


The **serverFiltering** must be used in conjunction with the **filter** configuration.  By default, a filter object is sent to the server with the query string in the following form:

*   filter[logic]: and
*   filter[filters][0][field]: orderId
*   filter[filters][0][operator]: desc
*   filter[filters][0][value]: 10248


Possible values for **operator** include:



##### *Equal To*

"eq", "==", "isequalto", "equals", "equalto", "equal"

##### *Not Equal To*

"neq", "!=", "isnotequalto", "notequals", "notequalto", "notequal", "ne"

##### *Less Then*

"lt", "<", "islessthan", "lessthan", "less"

##### *Less Then or Equal To*

"lte", "<=", "islessthanorequalto", "lessthanequal", "le"

##### *Greater Then*

"gt", ">", "isgreaterthan", "greaterthan", "greater"

##### *Greater Then or Equal To*

"gte", ">=", "isgreaterthanorequalto", "greaterthanequal", "ge"

##### *Starts With*

"startswith"

##### *Ends With*

"endswith"

##### *Contains*

"contains"


It is possible to modify these parameters by using the **parameterMap** function found on the **transport** object (see **transport** in Configuration).

#### Example

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: "orders.json"
        },
        serverFiltering: true,
        filter: { field: "orderId", operator: "eq", value: 10248 } // return only data where orderId equals 10248
    });

### serverGrouping `Boolean`*(default: false)*

 Determines if grouping of the data should be handled on the server.


The **serverGrouping** must be used in conjunction with the **group** configuration.  By default, a group object is sent to the server with the query string in the following form:

*   group[0][field]: orderId
*   group[0][dir]: desc


It is possible to modify these parameters by using the **parameterMap** function found on the **transport** object (see **transport** in Configuration).

#### Example

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: "orders.json"
        },
        serverGrouping: true,
        sort: { field: "orderId", dir: "asc" } // group by orderId descending
    });

### serverPaging `Boolean`*(default: false)*

 Determines if paging of the data should be handled on the server.


**serverPaging** must be used in conjunction with the **pageSize** configuration setting. The following options to the server as part of the query string by default:


##### *take*

contains the number of records to retreive

##### *skip*

how many records from the front of the dataset to begin reading

##### *page*

the index of the current page of data

##### *pageSize*

the number of records per page
<p>It is possible to modify these parameters by using the **parameterMap** function found on the **transport** object (see **transport** in Configuration).

#### Example

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: "orders.json"
        },
        serverPaging: true,
        pageSize: 5 // 5 records per page
    });

### serverSorting `Boolean`*(default: false)*

 Determines if sorting of the data should be handled on the server.


The **serverSorting** must be used in conjunction with the **sort** configuration.  By default, a sort object is sent to the server with the query string in the following form:

*   sort[0][field]: orderId
*   sort[0][dir]: asc


It is possible to modify these parameters by using the **parameterMap** function found on the **transport** object (see **transport** in Configuration).

#### Example

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: "orders.json"
        },
        serverSorting: true,
        sort: { field: "orderId", dir: "asc" }
    });

### sort `Array | Object`*(default: undefined)*

 Sets initial sort order

#### Example

    // sorts data ascending by orderId field
    sort: { field: "orderId", dir: "asc" }
    
    // sorts data ascending by orderId field and then descending by shipmentDate
    sort: [ { field: "orderId", dir: "asc" }, { field: "shipmentDate", dir: "desc" } ]

### transport `Object`

Sets the object responsible for loading and saving of data.
 This can be a remote or local/in-memory data.

### transport.create `Object | String`

Options for remote create data operation, or the URL of the remote service

#### Example

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: "orders.json",
            create: {
                url: "orders/create.json",
                data: {
                    orderId: $("#input").val() // sends the value of the input as the orderId
                }
            }
        }
    });

### transport.create.dataType `String`

The type of data that you're expecting back from the server

### transport.create.url `Object | String`

The remote url to call when creating a new record

### transport.destroy `Object | String`

Options for the remote delete data operation, or the URL of the remote service

### transport.destroy.dataType `String`

The type of data that you're expecting back from the server

### transport.destroy.url `Object | String`

The remote url to call when creating a new record

### transport.parameterMap `Function`

Convert the request parameters from dataSource format to remote service specific format.

#### Example

    var dataSource = new kendo.data.DataSource({
         transport: {
           read: "Catalog/Titles",
           parameterMap: function(options) {
              return {
                 pageIndex: options.page,
                 size: options.pageSize,
                 orderBy: convertSort(options.sort)
              }
           }
         }
     });

### transport.read `Object | String`

Options for remote read data operation, or the URL of the remote service

#### Example

    // settings various options for remote data transport
    var dataSource = new kendo.data.DataSource({
        transport: {
            read: {
                // the remote service URL
                url: "http://search.twitter.com/search.json",
    
                // JSONP is required for cross-domain AJAX
                dataType: "jsonp",
    
                // additional parameters sent to the remote service
                data: {
                    q: function() {
                        return $("#searchFor").val();
                    }
                }
            }
        }
    });
    
     // consuming odata feed without setting additional options
     var dataSource = new kendo.data.DataSource({
         type: "odata",
         transport: {
             read: "http://odata.netflix.com/Catalog/Titles"
         }
     });

### transport.read.data `Object | Function`

Additional data to be sent to the server

### transport.read.dataType `String`

The type of data that you're expecting back from the server

### transport.read.url `String`

The remote service URL

### transport.update `Object | String`

Options for remote update operation, or the URL of the remote service

#### Example

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: "orders.json",
            update: {
                url: "orders/update.json",
            }
        }
    });

### transport.update.dataType `String`

The type of data that you're expecting back from the server

### transport.update.url `Object | String`

The remote url to call when updating a record

### type `String`

Loads transport with preconfigured settings. Currently supports only "odata" (Requires kendo.data.odata.js to be included).

## Methods

### add

Adds a new Model instance to the DataSource

#### Example

    var model = kendo.data.Model.extend({
        id: "orderId",
        fields: {
            name: "customerName",
            description: "orderDescription",
            address: "customerAddress"
        }
    });
    // add a new model item to the data source.  If a model has not been declared as above, a new
    // model instance will be created for you.
    dataSource.add({ name: "John Smith", description: "Product Description", address: "123 1st Street" });

#### Parameters

##### model `Object`

Either a Model instance or raw object from which the Model will be created

#### Returns

`Object` The Model instance which has been added

### aggregate

Get current aggregate descriptors or applies aggregates to the data.

#### Example

    dataSource.aggregate({ field: "orderId", aggregate: "sum" });

#### Parameters

##### val `Object|Array`

_optional, default: _

<undefined> Aggregate(s) to be applied to the data.

#### Returns

`Array` Current aggregate descriptors

### aggregates

Get result of aggregates calculation

#### Example

    var aggr = dataSource.aggregates();

#### Returns

`Array` Aggregates result

### at

Returns the raw data record at the specified index

#### Example

    // returns the 4th item in the collection
    var order = dataSource.at(3);

#### Parameters

##### index `Number`

The zero-based index of the data record

#### Returns

`Object` 

### cancelChanges

Cancel the changes made to the DataSource after the last sync. Any changes currently existing in the model
will be discarded.

#### Example

    // we have updated 2 items and deleted 1. All of those changes will be discarded.
    dataSource.cancelChanges();

#### Parameters

##### model ``



### data

Get data returned from the transport

#### Example

    var data = dataSource.data();

#### Parameters

##### value ``



#### Returns

`Array` Array of items

### fetch

Fetches data using the current filter/sort/group/paging information.
If data is not available or remote operations are enabled data is requested through the transport,
otherwise operations are executed over the available data.

#### Example

    dataSource.fetch();

#### Parameters

##### callback ``



### filter

Get current filters or filter the data.



_Supported filter operators/aliases are_:


##### *Equal To*

"eq", "==", "isequalto", "equals", "equalto", "equal"

##### *Not Equal To*

"neq", "!=", "isnotequalto", "notequals", "notequalto", "notequal", "ne"

##### *Less Then*

"lt", "<", "islessthan", "lessthan", "less"

##### *Less Then or Equal To*

"lte", "<=", "islessthanorequalto", "lessthanequal", "le"

##### *Greater Then*

"gt", ">", "isgreaterthan", "greaterthan", "greater"

##### *Greater Then or Equal To*

"gte", ">=", "isgreaterthanorequalto", "greaterthanequal", "ge"

##### *Starts With*

"startswith"

##### *Ends With*

"endswith"

##### *Contains*

"contains", "substringof"

#### Example

    dataSource.filter({ field: "orderId", operator: "eq", value: 10428 });
    dataSource.filter([
         { field: "orderId", operator: "neq", value: 42 },
         { field: "unitPrice", operator: "ge", value: 3.14 }
    ]);

#### Parameters

##### val `Object|Array`

_optional, default: _

<undefined> Filter(s) to be applied to the data.

#### Returns

`Array` Current filter descriptors

### get

Retrieves a Model instance by given id.

#### Example

    var order = dataSource.get(1); // retrieves the "order" model item with an id of 1

#### Parameters

##### id `Number`

The id of the model to be retrieved

#### Returns

`Object` Model instance if found

### getByUid

Retrieves a Model instance by its UID.

#### Parameters

##### uid `String`

The uid of the record to be retrieved

#### Returns

`Object` Model instance if found

### group

Get current group descriptors or group the data.

#### Example

    dataSource.group({ field: "orderId" });

#### Parameters

##### val `Object|Array`

_optional, default: _

<undefined> Group(s) to be applied to the data.

#### Returns

`Array` Current grouping descriptors

### insert

Inserts a new Model instance to the DataSource.

#### Example

    var model = kendo.data.Model.extend({
        id: "orderId",
        fields: {
            name: "customerName",
            description: "orderDescription",
            address: "customerAddress"
        }
    });
    // insert a new model item at the very front of the collection
    dataSource.insert(0, { name: "John Smith", description: "Product Description", address: "123 1st Street" });

#### Parameters

##### index `Number`

Index at which the Model will be inserted

##### model `Object`

Either a Model instance or raw object from which the Model will be created

#### Returns

`Object` The Model instance which has been inserted

### page

Get current page index or request a page with specified index.

#### Example

    dataSource.page(2);

#### Parameters

##### val `Number`

_optional, default: _

<undefined> The index of the page to be retrieved

#### Returns

`Number` Current page index

### pageSize

Get current pageSize or request a page with specified number of records.

#### Example

    dataSource.pageSize(25);

#### Parameters

##### val `Number`

_optional, default: _

<undefined> The of number of records to be retrieved.

#### Returns

`Number` Current page size

### query

Executes a query over the data. Available operations are paging, sorting, filtering, grouping.
If data is not available or remote operations are enabled, data is requested through the transport.
Otherwise operations are executed over the available data.

#### Example

    
    // create a view containing at most 20 records, taken from the
    // 5th page and sorted ascending by orderId field.
    dataSource.query({ page: 5, pageSize: 20, sort: { field: "orderId", dir: "asc" } });
    
    // moves the view to the first page returning at most 20 records
    // but without particular ordering.
    dataSource.query({ page: 1, pageSize: 20 });

#### Parameters

##### options `Object`

_optional, default: _

Contains the settings for the operations. Note: If setting for previous operation is omitted, this operation is not applied to the resulting view

### read

Read the data into the DataSource using the transport read definition

#### Example

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: "orders.json";
        }
    });
    // the datasource will not contain any data until a read is called
    dataSource.read();

#### Parameters

##### data ``



### remove

Remove given Model instance from the DataSource.

#### Example

    // get the model item with an id of 1 from the DataSource
    var itemToRemove = dataSource.get(1);
    // remove the item from the DataSource
    dataSource.remove(itemToRemove);

#### Parameters

##### model `Object`

Model instance to be removed

### sort

Get current sort descriptors or sorts the data.

#### Example

    dataSource.sort({ field: "orderId", dir: "desc" });
    dataSource.sort([
         { field: "orderId", dir: "desc" },
         { field: "unitPrice", dir: "asc" }
    ]);

#### Parameters

##### val `Object | Array`

_optional, default: _

<undefined> Sort options to be applied to the data

#### Returns

`Array` Current sort descriptors

### sync

Synchronizes changes through the transport. Any pending CRUD operations will be sent to the server.
<p>If the DataSource is in **batch** mode, only one call will be made for each type of operation.
Otherwise, the DataSource will send one command per pending item change per change type.

#### Example

    // we have deleted 2 items and updated 1. If not in batch mode, this will send three commands to the server
    dataSource.sync();

### total

Get the total number of records

#### Example

    var total = dataSource.total();

### totalPages

Get the number of available pages.

#### Example

    var pages = dataSource.totalPages();

#### Returns

`Number` Number of available pages.

### view

Returns a view of the data with operation such as in-memory sorting, paring, grouping and filtering are applied.
To ensure that data is available this method should be use from within change event of the dataSource.

#### Example

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: "orders.json"
        }
        change: function(e) {
           // create a template instance
           var template = kendo.template($("#template").html());
           // render a view by passing the data to a template
           kendo.render(template, dataSource.view());
        }
    });

#### Returns

`Array` Array of items

## Events

### change

Fires when data is changed

#### Example

    var dataSource = new kendo.data.DataSource({
        change: function(e) {
            // handle event
        }
    });

#### To set after initialization

    dataSource.bind("change", function(e) {
        // handle event
    });

### error

Fires when an error occurs during data retrieval. The event arguments are the same as the ones of the error event of $.ajax().

#### Example

    var dataSource = new kendo.data.DataSource({
        error: function(e) {
            // handle event
        }
    });

#### To set after initialization

    dataSource.bind("error", function(e) {
        // handle event
    });

### requestStart

Fires when data request is to be made

#### Example

    var dataSource = new kendo.data.DataSource({
        requestStart: function(e) {
            // handle event
        }
    });

#### To set after initialization

    dataSource.bind("requestStart", function(e) {
        // handle event
    });

#### Event Data

##### e.sender `DataSource`

Reference to the dataSource object instance.