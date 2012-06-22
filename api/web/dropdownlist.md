---
title: kendo.ui.DropDownList
tags: api,web
publish: true
---

# kendo.ui.DropDownList

## Description



 A **DropDownList** displays a list of values and allows the selection of a single value from the
 list.Custom values may not be entered via keyboard input.If you wish permit keyboard input - that is, custom
 values are allowed - use the **ComboBox**.


### Getting Started

There are two ways to create a **DropDownList**:

1.  From a &lt;select&gt; element with HTML to define the list items
2.  From an &lt;input&gt; element with databinding to define the listitems



 A **DropDownList** will look and operate consistently regardless of the way in which it was
 created.

#### Creating a DropDownList from existing &lt;input&gt; element

    <input id="dropDownList" />

 Initialization of a **DropDownList** should occur after the DOM is fully loaded. It is recommended
 that initialization the **DropDownList** occur within a handler is provided to
 $(document).ready().

#### Initialize a DropDownList using a selector within $(document).ready()

    $(document).ready(function() {
        $("#dropDownList").kendoDropDownList({
            dataTextField: "text",
            dataValueField: "value",
            dataSource: [
                { text: "Item1", value: "1" },
                { text: "Item2", value: "2" }
            ]
        });
    });

#### Create a DropDownList from existing &lt;select&gt; element with a pre-defined structure

    <select id="dropDownList">
        <option>Item 1</option>
        <option>Item 2</option>
        <option>Item 3</option>
    </select>
    
    <script>
        $(document).ready(function(){
            $("#dropDownList").kendoDropDownList();
        });
    </script>

### Binding to Local or Remote Data


 The **DropDownList** can be bound to both local arrays and remote data via the
 **DataSource** component; an abstraction for local and
 remote data. Local arrays are appropriate for limited value options, while remote data binding is better for
 larger data sets. With remote data-binding, items will be loaded on-demand; when they are displayed.

#### Binding to a remote OData service

    $(document).ready(function() {
        $("#titles").kendoDropDownList({
            index: 0,
            dataTextField: "Name",
            dataValueField: "Id",
            dataSource: {
                type: "odata",
                transport: {
                    read: "http://odata.netflix.com/Catalog/Titles"
                }
            }
        });
    });



### Customizing Item Templates


 The **DropDownList** uses Kendo UI templates to enable you to control how items are rendered. For
 a detailed description of the capabilities and syntax of the Kendo UI templates, please refer to the
 [documentation](http://www.kendoui.com/documentation/framework/templates/overview.aspx "Kendo UI Template").

#### Basic item template customization

    <!-- HTML -->
    <input id="titles" />
    
    <!-- Template -->
    <script id="scriptTemplate" type="text/x-kendo-template">
        # if (data.BoxArt.SmallUrl) { #
            <img src="${ data.BoxArt.SmallUrl }" alt="${ data.Name }" />
            Title:${ data.Name }, Year: ${ data.Name }
        # } else { #
            <img alt="${ data.Name }" />
            Title:${ data.Name }, Year: ${ data.Name }
        # } #
    </script>
    
    <!-- DropDownList initialization -->
    <script type="text/javascript">
        $(document).ready(function() {
            $("#titles").kendoDropDownList({
                autoBind: false,
                dataTextField: "Name",
                dataValueField: "Id",
                template: $("#scriptTemplate").html(),
                dataSource: {
                    type: "odata",
                    transport: {
                        read: "http://odata.netflix.com/Catalog/Titles"
                    }
                }
            });
        });
    </script>

### Accessing an Existing DropDownList


 You can reference an existing **DropDownList** instance via
 [jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
 use the API to control its behavior.

#### Accessing an existing DropDownList instance

    var dropDownList = $("#dropDownList").data("kendoDropDownList");

## Configuration

### `animation` : **Object** 

 Animations to be used for opening/closing the popup. Setting to false will turn of the animation.

### `animation.close` : **Object** 

 Animation to be used for closing of the popup.

#### Example

    //dropdownlist initialization
     <script>
         $("#dropdownlist").kendoDropDownList({
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

### `animation.open` : **Object** 

 Animation to be used for opening of the popup.

#### Example

    //dropdownlist initialization
     <script>
         $("#dropdownlist").kendoDropDownList({
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

### `autoBind` : **Boolean** *(default: true)*

 Controls whether to bind the widget on initialization.

#### Example

    $("#dropdownlist").kendoDropDownList({
        autoBind: false
    });

### `dataSource` : **kendo.data.DataSource | Object** 

Instance of DataSource or the data that the DropDownList will be bound to.

#### Example

    // bind to local data
    var items = [ { Id: 0, Title: "Manager" }, { Id: 1, Title: "Developer" }, { Id: 2, Title: "Vice President" } ];
    $("#dropdownlist").kendoDropDownList({
        dataSource: items,
        dataTextField: "Title",
        dataValueField: "Id"
    });

#### Example

    $("#dropdownlist").kendoDropDownList({
        dataSource: {
            transport: {
                read: "titles.json"
            }
        },
        dataTextField: "Title",
        dataValueField: "Id"
    });

### `dataTextField` : **String** *(default: "")*

 Sets the field of the data item that provides the text content of the list items.

#### Example

    var items = [ { Id: 0, Title: "Manager" }, { Id: 1, Title: "Developer" }, { Id: 2, Title: "Vice President" } ];
    $("#dropdownlist").kendoDropDownList({
        dataSource: items,
        dataTextField: "Title",
        dataValueField: "Id"
    });

### `dataValueField` : **String** *(default: "")*

 Sets the field of the data item that provides the value content of the list items.

#### Example

    var items = [ { Id: 0, Title: "Manager" }, { Id: 1, Title: "Developer" }, { Id: 2, Title: "Vice President" } ];
    $("#dropdownlist").kendoDropDownList({
        dataSource: items,
        dataTextField: "Title",
        dataValueField: "Id"
    });

### `delay` : **Number** *(default: 500)*

 Specifies the delay in ms before the search text typed by the end user is cleared.

#### Example

    $("#dropdownlist").kendoDropDownList({
        delay: 1000 // wait 1 second before clearing the user input
    });

### `enable` : **Boolean** *(default: true)*

 Controls whether the DropDownList should be initially enabled.

#### Example

    $("#dropdownlist").kendoDropDownList({
        enabled: false // dropdown list will not be enabled
    });

#### Example

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    // disable the dropdown
    dropdownlist.enable(false);

### `height` : **Number** *(default: 200)*

 Define the height of the drop-down list in pixels.

#### Example

    $("#dropdownlist").kendoDropDownList({
        height: 400
    });

### `ignoreCase` : **String** *(default: true)*

 Controls whether the search should be case sensitive.

#### Example

    $("#dropdownlist").kendoDropDownList({
        ignoreCase: false //now search will be case sensitive
    });

### `index` : **Number** *(default: 0)*

 Defines the initial selected item.

#### Example

    $("#dropdownlist").kendoDropDownList({
        index: 1 // selects the second item in the dropdown list
    });

### `optionLabel` : **String | Object** *(default: "")*

 Define the text of the default empty item. If the value is an object, then the widget will use it directly.

#### Example

    $("#dropdownlist").kendoDropDownList({
        optionLabel: "Select An Option"
    });

#### Example

    $("#dropdownlist").kendoDropDownList({
        dataTextField: "text",
        dataValueField: "value",
        optionLabel: {
           text: "Select An Option",
           value: ""
        }
    });

### `template` : **String** 

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
    
     //dropdownlist initialization
     <script>
         $("#dropdownlist").kendoDropDownList({
             dataSource: dataSource,
             dataTextField: "Name",
             dataValueField: "Id",
             template: kendo.template($("#template").html())
         });
     </script>

### `text` : **String** *(default: "")*

 Define the text of the widget, when the autoBind is set to false.

#### Example

    $("#dropdownlist").kendoDropDownList({
         autoBind: false,
         text: "Chai"
    });

### `value` : **String** *(default: "")*

 Define the value of the widget

#### Example

    $("#dropdownlist").kendoDropDownList({
         dataSource: ["Item1", "Item2"],
         value: "Item1"
    });

## Methods

### close

Closes the drop-down list.

#### Example

    // get a reference to the dropdown widget
    var dropdownList = $("#dropdownList").data("kendoDropDownList");
    // close the dropdown
    dropdownlist.close();

### dataItem

Returns the raw data record at the specified index. If the index is not specified, the selected index will be used.

#### Example

    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    
    // get the dataItem corresponding to the selectedIndex.
    var dataItem = dropdownlist.dataItem();
    
    // get the dataItem corresponding to the passed index.
    var dataItem = dropdownlist.dataItem(1);

#### Parameters

##### index `Number`

The zero-based index of the data record

#### Returns

`Object` The raw data record. Returns <i>undefined</i> if no data.

### enable

Enables/disables the dropdownlist widget

#### Example

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    // disable the dropdown list
    dropdownlist.enable(false);

#### Parameters

##### enable `Boolean`

Desired state

### open

Opens the drop-down list.

#### Example

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    // open the drop down
    dropdownlist.open();

### refresh

Re-render the items in drop-down list.

#### Example

    // get a referenence to the Kendo UI DropDownList
    var dropdownlist = $("dropdownlist").data("kendoDropDownList");
    // re-render the items in drop-down list.
    dropdownlist.refresh();

### search

Selects item, which starts with the provided parameter.

#### Example

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    
    // Selects item which starts with "In".
    dropdownlist.search("In");

#### Parameters

##### word `string`

The search value.

### select

Selects drop-down list item and sets the value and the text of the dropdownlist.

#### Example

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    
    // selects by jQuery object
    dropdownlist.select(dropdownlist.ul.children().eq(0));
    
    // selects by index
    dropdownlist.select(1);
    
    // selects item if its text is equal to "test" using predicate function
    dropdownlist.select(function(dataItem) {
        return dataItem.text === "test";
    });

#### Parameters

##### li `jQuery | Number | Function`

LI element or index of the item or predicate function, which defines the item that should be selected.

#### Returns

`Number` The index of the selected LI element.

### text

Gets/Sets the text of the dropdownlist.

#### Example

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    
    // get the text of the dropdownlist.
    var text = dropdownlist.text();

#### Parameters

##### text `String`

The text to set.

#### Returns

`String` The text of the dropdownlist.

### toggle

Toggles the drop-down list between opened and closed state.

#### Example

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    
    // toggles the open state of the drop-down list.
    dropdownlist.toggle();

#### Parameters

##### toggle `Boolean`

Defines the whether to open/close the drop-down list.

### value

Gets/Sets the value of the dropdownlist. The value will not be set if there is no item with such value. If value is undefined, text of the data item is used.

#### Example

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    
    // get the value of the dropdownlist.
    var value = dropdownlist.value();
    
    // set the value of the dropdownlist.
    dropdownlist.value("1"); //looks for item which has value "1"

#### Parameters

##### value `String`

The value to set.

#### Returns

`String` The value of the dropdownlist.

## Events

### change

Fires when the value has been changed.

#### Example

    $("#dropdownlist").kendoDropDownList({
        change: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    // bind to the change event
    dropdownlist.bind("change", function(e) {
        // handle event
    });

### close

Fires when the drop-down list is closed

#### Example

    $("#dropdownlist").kendoDropDownList({
        close: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    // bind to the close event
    dropdownlist.bind("close", function(e) {
        // handle event
    });

### open

Fires when the drop-down list is opened

#### Example

    $("#dropdownlist").kendoDropDownList({
        open: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the dropdown list
    var dropdownlist = $("#dropdownlist").data("kendoDropDownList");
    // bind to the open event
    dropdownlist.bind("open", function(e) {
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
    var dropdownlist = $("#dropdownlist").kendoDropDownList({
        select: onSelect
    });
    
    // detach select event handler via unbind()
    dropdownlist.data("kendoDropDownList").unbind("select", onSelect);

#### Attach select event handler via bind(); detach via unbind()

    // event handler for select
    var onSelect = function(e) {
        // access the selected item via e.item (jQuery object)
    };
    
    // attach select event handler via bind()
    $("#dropdownlist").data("kendoDropDownList").bind("select", onSelect);
    
    // detach select event handler via unbind()
    $("#dropdownlist").data("kendoDropDownList").unbind("select", onSelect);

#### Event Data

##### e.item `jQuery`

The selected item chosen by a user.