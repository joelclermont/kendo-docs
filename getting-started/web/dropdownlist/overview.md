---
title: DropDownList Overview
slug: gs-web-dropdownlist-overview
tags: getting-started,web
publish: true
---

# DropDownList Overview

A **DropDownList** displays a list of values and allows the selection of a single value from the
list.Custom values may not be entered via keyboard input.If you wish permit keyboard input - that is, custom
values are allowed - use the **ComboBox**.


## Getting Started

There are two ways to create a **DropDownList**:

1.  From a &lt;select&gt; element with HTML to define the list items
2.  From an &lt;input&gt; element with databinding to define the listitems



A **DropDownList** will look and operate consistently regardless of the way in which it was
created.

### Creating a DropDownList from existing &lt;input&gt; element

    <input id="dropDownList" />

Initialization of a **DropDownList** should occur after the DOM is fully loaded. It is recommended
that initialization the **DropDownList** occur within a handler is provided to
$(document).ready().

### Initialize a DropDownList using a selector within $(document).ready()

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

### Create a DropDownList from existing &lt;select&gt; element with a pre-defined structure

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

## Binding to Local or Remote Data


The **DropDownList** can be bound to both local arrays and remote data via the
**DataSource** component; an abstraction for local and
remote data. Local arrays are appropriate for limited value options, while remote data binding is better for
larger data sets. With remote data-binding, items will be loaded on-demand; when they are displayed.

### Binding to a remote OData service

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



## Customizing Item Templates


The **DropDownList** uses Kendo UI templates to enable you to control how items are rendered. For
a detailed description of the capabilities and syntax of the Kendo UI templates, please refer to the
[documentation](http://www.kendoui.com/documentation/framework/templates/overview.aspx "Kendo UI Template").

### Basic item template customization

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

## Accessing an Existing DropDownList


You can reference an existing **DropDownList** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

### Accessing an existing DropDownList instance

    var dropDownList = $("#dropDownList").data("kendoDropDownList");

