---
title: ComboBox Overview
slug: getting-started.web.combobox
tags: getting-started,web
publish: true
---

# ComboBox Overview

The **ComboBox** displays a list of values and allows the selection of a single value from this
list. Custom values may also be entered via keyboard input. If you do not wish permit keyboard input - that is,
custom values are not permitted - use the **DropDownList**.

The **ComboBox** represents a richer version of a `<select>` element, providing support for
local and remote data binding, item templates, and configurable options for controlling the list behavior.


## Getting Started

There are two ways to create a **ComboBox**:

1.  From a `<select>` element with HTML to define the list items
2.  From an `<input>` element with databinding to define the listitems



A **ComboBox** will look and operate consistently regardless of the way in which it was created.

### Creating a ComboBox from an existing &lt;input&gt; element

    <input id="comboBox" />

Initialization of a **ComboBox** should occur after the DOM is fully loaded. It is recommended
that initialization the **ComboBox** occur within a handler is provided to
$(document).ready().

### Initialize a ComboBox using a selector within $(document).ready()

    $(document).ready(function(){
        $("#comboBox").kendoComboBox({
            dataTextField: "text",
            dataValueField: "value",
            dataSource: [
                { text: "Item1", value: "1" },
                { text: "Item2", value: "2" }
            ]
        });
    });

### Creating a ComboBox from existing `<select>` element with a pre-defined structure

    <select id="comboBox">
        <option>Item 1</option>
        <option>Item 2</option>
        <option>Item 3</option>
    </select>

    <script>
        $(document).ready(function(){
            $("#comboBox").kendoComboBox();
        });
    </script>

## Binding to Local or Remote Data


The **ComboBox** can be bound to both local arrays and remote data via the
**DataSource** component; an abstraction for local and
remote data. Local arrays are appropriate for limited value options, while remote data binding is better for
larger data sets. With remote data-binding, items will be loaded on-demand; when they are displayed.

### Binding to a remote OData service

    $(document).ready(function() {
        $("#comboBox").kendoComboBox({
            index: 0,
            dataTextField: "Name",
            dataValueField: "Id",
            filter: "contains",
            dataSource: {
                type: "odata",
                serverFiltering: true,
                serverPaging: true,
                pageSize: 20,
                transport: {
                    read: "http://odata.netflix.com/Catalog/Titles"
                }
            }
        });
    });

## Customizing Item Templates


The **ComboBox** uses Kendo UI templates to enable you to control how items are rendered. For a
detailed description of the capabilities and syntax of the Kendo UI templates, please refer to the
[documentation](http://www.kendoui.com/documentation/framework/templates/overview.aspx "Kendo UI Template").

### Basic item template customization

    <input id="comboBox" />
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

    <!-- ComboBox initialization -->
    <script>
        $(document).ready(function() {
            $("#comboBox").kendoComboBox({
                autoBind: false,
                dataTextField: "Name",
                dataValueField: "Id",
                template: $("#scriptTemplate").html(),
                dataSource: {
                    type: "odata",
                    serverFiltering: true,
                    serverPaging: true,
                    pageSize: 20,
                    transport: {
                        read: "http://odata.netflix.com/Catalog/Titles"
                    }
                }
            });
        });
    </script>

## Accessing an Existing ComboBox


You can reference an existing **ComboBox** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Objectnce a reference has been established, you
can use the API to control its behavior.

### Accessing an existing ComboBox instance

    var comboBox = $("#comboBox").data("kendoComboBox");

