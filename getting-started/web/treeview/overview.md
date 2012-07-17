---
title: TreeView Overview
slug: gs-web-treeview-overview
tags: getting-started,web
publish: true
---

# TreeView Overview

The **TreeView** displays hierarchical data in a traditional tree structure. It supports user
interaction through the mouse or touch to perform re-ordering operations via drag-and-drop.



A **TreeView** can be created by leveraging HTML lists. However, it does not support binding to a
remote data source at this point in time.


## Getting Started

A **TreeView** can be created in two ways:

1.  Define a hierarchical list with static HTML
2.  Use dynamic data binding



Static HTML definition is appropriate for small hierarchies and for data that does not change frequently.
Databinding should be used for larger data sets and for data that changes frequently.


## Creating a TreeView from HTML

### Create a hierarchical list in HTML

    <ul id="treeView">
        <li>Item 1
            <ul>
                <li>Item 1.1</li>
                <li>Item 1.2</li>
            </ul>
        </li>
        <li>Item 2</li>
    </ul>

Initialization of a **TreeView** should occur after the DOM is fully loaded. It is recommended
that initialization the **TreeView** occur within a handler is provided to $(document).ready().

### Initialize a TreeView using a selector within $(document).ready()

    $(document).ready(function() {
        $("#treeView").kendoTreeView();
    });

## Creating a TreeView with Data Binding to a Local Data Source

### Create a hierarchical HTML list

    <div id="treeView"></div>

### Initialize and bind the TreeView

    $(document).ready(function() {
        $("#treeView").kendoTreeView({
            dataSource: [
                {
                    text: "Item 1",
                    items: [
                        { text: "Item 1.1" },
                        { text: "Item 1.2" }
                    ]
                },
                { text: "Item 2" }
            ]
        })
    });

### Binding to remote HierarchicalDataSource

    $("#treeView").kendoTreeView({
        dataSource: {
            transport: {
                read: {
                    url: "http://demos.kendoui.com/service/Employees",
                    dataType: "json"
                }
            },
            schema: {
                model: {
                    id: "EmployeeId",
                    hasChildren: "HasEmployees"
                }
            }
        }
    })

A complete reference on how to bind the TreeView to different service end-points can be found
on the [HierarchicalDataSource API help](/api/framework/hierarchicaldatasource).

### Default item JSON structure

    var item = {
        text: "Item text",

        // renders a <img class="k-image" src="/images/icon.png" />
        imageUrl: "/images/icon.png",

        // renders a <span class="k-sprite icon save" />
        spriteCssClass: "icon save",

        // specifies whether the node text should be encoded or not
        // useful when rendering node-specific HTML
        encoded: false
    };

A number of **TreeView** behaviors can be easily controlled by simple configuration properties,
such as animation behaviors and drag-and-drop behaviors.

### Enabling drag-and-drop for TreeView nodes

    $("#treeView").kendoTreeView({
        dragAndDrop: true
    });

When drag-and-drop is enabled, the nodes of a **TreeView** can be dragged and dropped between all
levels, with useful tooltips helping indicate where the node will be dropped.


## Accessing an Existing TreeView


You can reference an existing **TreeView** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

### Accessing an existing TreeView instance

    var treeView = $("#treeView").data("kendoTreeView");

