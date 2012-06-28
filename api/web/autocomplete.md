---
title: kendo.ui.AutoComplete
tags: api,web
publish: true
---

# kendo.ui.AutoComplete

## Description



The **AutoComplete** provides suggestions depending on the typed
text. It also allows multiple value entries. The suggestions shown by
the **AutoComplete** can come from a local Array or from a remote
data service.


### Getting Started

#### Create a HTML input element

    <input id="autoComplete" />

#### Initialize the AutoComplete using a jQuery selector

    $(document).ready(function() {
     $("#autoComplete").kendoAutoComplete(["Item1", "Item2"]);
    });

### AutoComplete Suggestions


There are two primary ways to provide the **AutoComplete**
suggestions:


1.  From a local array
2.  From a remote data service



Locally defined values are best for small, fixed sets of suggestions.
Remote suggestions should be used for larger data sets. When used
with the **DataSource** component,
filtering large remote data services can be pushed to the server as
well, maximizing client-side performance.


### Local Suggestions


To configure and provide **AutoComplete** suggestions locally, you
can either pass an array directly to its constructor or you can set
the dataSource property to an local array.

#### Directly initialize suggestions in constructor

    $("#autoComplete").kendoAutoComplete(["Item1", "Item2", "Item3"]);

#### Using dataSource property to bind to local Array

    var data = ["Item1", "Item2", "Item3"];
    $("#autoComplete").kendoAutoComplete({
       dataSource: data
    });

### Remote Suggestions


The easiest way to bind an **AutoComplete** to remote
suggestions is to use the
**DataSource** component; an
abstraction for local and remote data. The **DataSource**
component can be used to serve data from a variety of data services,
such as
[XML](http://en.wikipedia.org/wiki/XML),
[JSON](http://en.wikipedia.org/wiki/JSON), and
[JSONP](http://en.wikipedia.org/wiki/JSONP).

#### Using the Kendo UI Web DataSource component to bind to
remote suggestions with OData

    $(document).ready(function(){
     $("#autoComplete").kendoAutoComplete({
      minLength: 3,
      dataTextField: "Name", // JSON property name to use
      dataSource: new kendo.data.DataSource({
       type: "odata", // specifies data protocol
       pageSize: 10, // limits result set
       transport: {
        read: "http://odata.netflix.com/Catalog/Titles"
       }
      })
     })
    });

#### Using the Kendo UI Web DataSource to bind to JSONP
suggestions

    $(document).ready(function(){
     $("#autoComplete").kendoAutoComplete({
      minLength:6,
      dataTextField:"title",
      filter: "contains",
      dataSource: new kendo.data.DataSource({
       transport: {
        read: {
         url: "http://api.geonames.org/wikipediaSearchJSON",
         data: {
          q: function(){
           return $("#autoComplete").data("kendoAutoComplete").value();
          },
          maxRows: 10,
          username: "demo"
         }
        }
       },
       schema: {
        data:"geonames"
       }
      }),
      change: function(){
       this.dataSource.read();
      }
     })
    });

### Accessing an Existing AutoComplete


You can reference an existing **AutoComplete** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the API to control
its behavior.

#### Accessing an existing AutoComplete instance

    var autoComplete = $("#autoComplete").data("kendoAutoComplete");

## Configuration

### animation `Object`

 Animations to be used for opening/closing the popup. Setting to false will turn of the animation.

### animation.close `Object`

 Animation to be used for closing of the popup.

#### Example

    //autocomplete initialization
     <script>
         $("#autocomplete").kendoAutoComplete({
             dataSource: dataSource,
             animation: {
                close: {
                    effects: "fadeOut",
                    duration: 300,
                    hide: true
                    show: false
                }
             }
         });
     </script>

### animation.open `Object`

 Animation to be used for opening of the popup.

#### Example

    //autocomplete initialization
     <script>
         $("#autocomplete").kendoAutoComplete({
             dataSource: dataSource,
             animation: {
                open: {
                    effects: "fadeIn",
                    duration: 300,
                    show: true
                }
             }
         });
     </script>

### dataSource `Object | kendo.data.DataSource`

The set of data that the AutoComplete will be bound to.
 Either a local JavaScript object, or an instance of the Kendo UI DataSource.

#### Example

    var items = [ { Name: "Item 1" }, { Name: "Item 2"} ];
    $("#autoComplete").kendoAutoComplete({ dataSource: items });

#### Example

    $("#autocomplete").kendoAutoComplete({
        dataSource: new kendo.data.DataSource({
            transport: {
                read: "Items/GetData" // url to server method which returns data
            }
        });
    });

### dataTextField `String`*(default: null)*

 Sets the field of the data item that provides the text content of the list items.

#### Example

    var items = [ { ID: 1, Name: "Item 1" }, { ID: 2, Name: "Item 2"} ];
    $("#autoComplete").kendoAutoComplete({
        dataSource: items,
        dataTextField: "Name"
    });

### delay `Number`*(default: 200)*

 Specifies the delay in ms after which the AutoComplete will start filtering the dataSource.

#### Example

    // set the delay to 500 milliseconds
    $("#autoComplete").kendoAutoComplete({
        delay: 500
    });

### enable `Boolean`*(default: true)*

 Controls whether the AutoComplete should be initially enabled.

#### Example

    // disable the autocomplete when it is created (enabled by default)
    $("#autoComplete").kendoAutoComplete({
        enable: false
    });

### filter `String`*(default: "startswith")*

 Defines the type of filtration. This value is handled by the remote data source.

#### Example

    // send a filter value of 'contains' to the server
    $("#autoComplete").kendoAutoComplete({
        filter: 'contains'
    });

### height `Number`*(default: 200)*

 Sets the height of the drop-down list in pixels.

#### Example

    // set the height of the drop-down list that appears when the autocomplete is activated to 500px
    $("#autoComplete").kendoAutoComplete({
        height: 500
    });

### highlightFirst `Boolean`*(default: true)*

 Controls whether the first item will be automatically highlighted.

#### Example

    $("#autocomplete").kendoAutoComplete({
        highlightFirst: false //no of the suggested items will be highlighted
    });

### ignoreCase `String`*(default: true)*

 Defines whether the filtration should be case sensitive.

#### Example

    $("#autoComplete").kendoAutoComplete({
        filter: 'contains',
        ignoreCase: false //now filtration will be case sensitive
    });

### minLength `Number`*(default: 1)*

 Specifies the minimum number of characters that should be typed before the AutoComplete queries
the dataSource.

#### Example

    // wait until the user types 3 characters before querying the server
    $("#autoComplete").kendoAutoComplete({
        minLength: 3
    });

### placeholder `String`*(default: "")*

 A string that appears in the textbox when it has no value.
 

#### Example

    //autocomplete initialization
     <script>
         $("#autocomplete").kendoAutoComplete({
             dataSource: dataSource,
             placeholder: "Enter value..."
         });
     </script>

#### Example

    <input id="autocomplete" placeholder="Enter value..." />
    
     //combobox initialization
     <script>
         $("#autocomplete").kendoAutoComplete({
             dataSource: dataSource
         });
     </script>

### separator `String`*(default: "")*

 Sets the separator for completion. Empty by default, allowing for only one completion.

#### Example

    // set completion separator to ,
    $("#autoComplete").kendoAutoComplete({
        separator: ", "
    });

### suggest `Boolean`*(default: false)*

 Controls whether the AutoComplete should automatically auto-type the rest of text.

#### Example

    // turn on auto-typing (off by default)
    $("#autoComplete").kendoAutoComplete({
        suggest: true
    });

### template `String`

Template to be used for rendering the items in the list.

#### Example

    //template
    
    <script id="template" type="text/x-kendo-tmpl">
          # if (data.BoxArt.SmallUrl) { #
              <img src="${ data.BoxArt.SmallUrl }" alt="${ data.Name }" />Title:${ data.Name }, Year: ${ data.Name }
          # } else { #
              <img alt="${ data.Name }" />Title:${ data.Name }, Year: ${ data.Name }
          # } #
     </script>
    
     //autocomplete initialization
     <script>
         $("#autocomplete").kendoAutoComplete({
             dataSource: dataSource,
             dataTextField: "Name",
             template: kendo.template($("#template").html())
         });
     </script>

## Methods

### close

Closes the drop-down list.

#### Example

    // get a reference to the autocomplete widget
    var autocomplete = $("autocomplete").data("kendoAutoComplete");
    
    autocomplete.close();

### dataItem

Returns the raw data record at the specified index

#### Example

    var autocomplete = $("#autocomplete").data("kendoAutoComplete");
    
    // get the dataItem corresponding to the passed index.
    var dataItem = autocomplete.dataItem(1);

#### Parameters

##### index `Number`

The zero-based index of the data record

#### Returns

`Object` The raw data record. Returns <i>undefined</i> if no data.

### enable

Enable/Disable the autocomplete widget.

#### Example

    // get a reference to the autocomplete widget
    var autocomplete = $("autocomplete").data("kendoAutoComplete");
    
    // disables the autocomplete
    autocomplete.enable(false);
    
    // enables the autocomplete
    autocomplete.enable(true);

#### Parameters

##### enable `Boolean`

The argument, which defines whether to enable/disable the autocomplete.

### refresh

Re-render the items in drop-down list.

#### Example

    // get a referenence to the Kendo UI AutoComplete
    var autocomplete = $("autocomplete").data("kendoAutoComplete");
    // re-render the items in drop-down list.
    autocomplete.refresh();

### search

Filters dataSource using the provided parameter and rebinds drop-down list.

#### Example

    // get a reference to the autocomplete widget
    var autocomplete = $("autocomplete").data("kendoAutoComplete");
    
    // Searches for item which has "Inception" in the name.
    autocomplete.search("Inception");

#### Parameters

##### word `string`

The filter value.

### select

Selects drop-down list item and sets the text of the autocomplete.

#### Example

    // get a reference to the autocomplete widget
    var autocomplete = $("autocomplete").data("kendoAutoComplete");
    
    // selects by jQuery object
    autocomplete.select(autocomplete.ul.children().eq(0));

#### Parameters

##### li `jQuery Object`

The LI element.

### suggest

Forces a suggestion onto the text of the AutoComplete.

#### Example

    // note that this suggest is not the same as the configuration method
    // suggest which enables/disables auto suggesting for the AutoComplete
    //
    // get a referenence to the Kendo UI AutoComplete
    var autoComplete = $("#autoComplete").data("kendoAutoComplete");
    
    // force a suggestion to the item with the name "Inception"
    autoComplete.suggest("Inception");

#### Parameters

##### value `string`

Characters to force a suggestion.

### value

Gets/Sets the value of the autocomplete.

#### Example

    // get a reference to the autocomplete widget
    var autocomplete = $("autocomplete").data("kendoAutoComplete");
    
    // get the text of the autocomplete.
    var value = autocomplete.value();

#### Parameters

##### value `String`

The value to set.

#### Returns

`String` The value of the autocomplete.

## Events

### change

Fires when the value has been changed.

#### To set after initialization

    var autoComplete = $("#autoComplete").data("kendoAutoComplete");
    $("#autoComplete").data("kendoAutoComplete").bind("change", function(e) {
        // handle event
    });

### close

Fires when the drop-down list is closed

#### Example

    $("#autoComplete").kendoAutoComplete({
        close: function(e) {
            // handle event
        }
    });

#### To set after initialization

    var autoComplete = $("#autoComplete").data("kendoAutoComplete");
    autoComplete.bind("close", function(e) {
        // handle event
    });

### open

Fires when the drop-down list is opened

#### Example

    $("#autoComplete").kendoAutoComplete({
        open: function(e) {
            // handle event
        }
    });

#### Example

    var autoComplete = $("#autoComplete").data("kendoAutoComplete");
    autoComplete.bind("open", function(e) {
        // handle event
    });

### select

Triggered when a Li element is selected.

#### Attach select event handler during initialization; detach via unbind()

    // event handler for select
    var onSelect = function(e) {
        // access the selected item via e.item (jQuery object)
    };
    
    // attach select event handler during initialization
    var autocomplete = $("#autocomplete").kendoAutoComplete({
        select: onSelect
    });
    
    // detach select event handler via unbind()
    autocomplete.data("kendoAutoComplete").unbind("select", onSelect);

#### Attach select event handler via bind(); detach via unbind()

    // event handler for select
    var onSelect = function(e) {
        // access the selected item via e.item (jQuery object)
    };
    
    // attach select event handler via bind()
    $("#autocomplete").data("kendoAutoComplete").bind("select", onSelect);
    
    // detach select event handler via unbind()
    $("#autocomplete").data("kendoAutoComplete").unbind("select", onSelect);

#### Event Data

##### e.item `jQuery`

The selected item chosen by a user.