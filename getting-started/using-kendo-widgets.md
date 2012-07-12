---
title:  Using Kendo Widgets
slug: gs-using-kendo-widgets
tags:   101, Getting Started, widgets
Publish:    true
related:    gs-downloading-kendo
---

# Using Kendo UI Widgets

## Widget initialization

Since Kendo UI is built on top of jQuery, using the Kendo UI widgets is very intuitive.
For example, to use Kendo AutoComplete, first you write some HTML:

    <input id="myAutoComplete" />

Then, to initialize this HTML input and give it the Kendo AutoComplete functionality and styling, a single jQuery JavaScript line is required:

    $("#myAutoComplete").kendoAutoComplete(["Apples", "Oranges", "Grapes"]);

## Widget configuration

To set additional configuration on widgets you can provide a JavaScript object to the widget constructor.

      $("#grid").kendoGrid({
          columns:[
              {
                  field: "FirstName",
                  title: "First Name"
              },
              {
                  field: "LastName",
                  title: "Last Name"
          }],
          dataSource: {
              data: [
                  {
                      FirstName: "Joe",
                      LastName: "Smith"
                  },
                  {
                      FirstName: "Jane",
                      LastName: "Smith"
              }]
          }
      });

The specific property names and configuration options for each widget can be found in the [API reference](jhttp://docs.kendoui.com/api) section of this site.

## Getting the widget client object

The widget client object is preserved in the jQuery [data store](http://docs.jquery.com/core/data "jQuery data store") for the corresponding element.
The following code snippet shows how to get the client object of the grid widget.

    var grid = $("#grid").data("kendoGrid");

> The name of the data key is built by adding "kendo" prefix to the widget's name

## Widget event binding

There are two ways to subscribe to Kendo UI widget events:

*   Provide a handler in the configuration during widget initialization
*   Using the **bind** method

### Subscribing during widget initialization

     $("#products").kendoAutoComplete({
        change: onChange,
        close: onClose,
        open: onOpen
    });


### Subscribing via the `bind` method

    var autoComplete = $("#products");
    autoComplete.bind("change", onChange);

The handler is a callback function, as shown below. Within the handler, the keyword `this` refers to the Kendo widget to which the handler is subscribed.

    <script>
     function onChange(args) {
          //"this" refers to the AutoComplete widget that triggers the event

          console.log(this.value()); // outputs the value of the widget
     }
    </script>


## Declarative widget initialization based on data attributes

In addition to the jQuery plugin initialization, each kendo widget can be initialized and configured by setting a `role` data attribute
on the target element and calling `kendo.init` on its element or any of its containers.

### Initialize a kendo DropDownList using a role attribute

    <div id="container">
        <select data-role="dropdownlist"></select>
    </div>
    <script>
        kendo.init($("#container"));
    </script>

The role attribute value is the name of the widget in lower case.

### Configuration

Each widget configuration option can be specified via a data attribute on the respective element.
Camel-cased options are translated to dash separated attributes. For instance, dataTextField option of the autocomplete widget can be specified with `data-text-field="foo"` attribute.

> Options, which start with `data` do not require an additional "data" in the attribute name. 

### Configure kendo DropDownList with data attributes

    <select data-role="dropdownlist" data-delay="1000">
    </select>

### Events / DataSource

A widget event can be bound using data attributes as well. The value of the data attribute will be resolved to a function, available in the global scope.

#### Bind to dropDownList change event

    <select data-role="dropdownlist" data-change="onChange">
    </select>
    <script>
        function onChange(e) {
            // ...
        }
    </script>

Event handlers also support member functions, using JavaScript syntax. An event handler can be specified using `foo.bar`, resolving to the member method `bar` of the object `foo`.

#### Bind to dropDownList change event to a member function

    <select data-role="dropdownlist" data-change="foo.bar">
    </select>
    <script>
    var foo = {
        bar: function(e) {
            // ...
        }
    }
    </script>

The declarative DataSource binding works in the same way, expecting a DataSource object or an array.


#### Specify DropDownList DataSource

    <select data-role="dropdownlist" data-source="source">
    </select>
    <script>
        var source = ["foo", "bar", "baz"];
    </script>

### Templates

For widgets that have template configuration options, the data attribute value will be resolved to an `id` of a `script`
element, with the contents of the template.

#### Specify DropDownList Template

    <select data-role="dropdownlist" data-template="foo"></select>

    <script id="foo" type="script/x-kendo-template">
        <span>#:data.Name</span>
    </script>

