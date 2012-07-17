---
title: Menu Overview
slug: getting-started.web.menu
tags: getting-started,web
publish: true
---

# Menu Overview

The **Menu** displays hierarchical data as a multi-level menu. It provides rich styling for unordered lists
of items, and can be used for both navigation and executing JavaScript commands. Items can be defined and
initialized from HTML, or the API can be used to add and remove items.


## Getting Started

### Create a HTML hierarchical list of items

    <ul id="menu">
        <li>Item 1
            <ul>
                <li>Item 1.1</li>
                <li>Item 1.2</li>
            </ul>
        </li>
        <li>Item 2</li>
    </ul>

Initialization of a **Menu** should occur after the DOM is fully loaded. It is recommended that
initialization the **Menu** occur within a handler is provided to $(document).ready().

### Initialize a Menu using a selector within $(document).ready()

    $(document).ready(function() {
        $("#menu").kendoMenu();
    });

### Initialize the Menu using JSON data object

    $(document).ready(function() {
     $("#menu").kendoMenu({
      dataSource:
        [{
            text: "Item 1",
            url: "http://www.kendoui.com"                // Link URL if navigation is needed, optional.
        },
        {
            text: "<b>Item 2</b>",
            encoded: false,                                 // Allows use of HTML for item text
            content: "text"                                 // content within an item
        },
        {
            text: "Item 3",
            imageUrl: "http://www.kendoui.com/test.jpg", // Item image URL, optional.
            items: [{                                    // Sub item collection
                 text: "Sub Item 1"
            },
            {
                 text: "Sub Item 2"
            }]
        },
        {
            text: "Item 4",
            spriteCssClass: "imageClass3"                // Item image sprite CSS class, optional.
        }]
     })
    });

## Customizing Menu Animations


By default, the **Menu** uses a slide animation to expand and
reveal sub-items as the mouse hovers. Animations can be easily
customized using configuration properties, changing the animation
style and delay. Menu items can also be configured to open on click
instead of on hover.

### Changing Menu animation and open behavior

    $("#menu").kendoMenu({
        animation: {
            open: { effects: "fadeIn" },
            hoverDelay: 500
        },
        openOnClick: true
    });

## Dynamically configuring Menu items


The **Menu** API provides several methods for dynamically adding
or removing Items. To add items, provide the new item as a JSON
object along with a reference item that will be used to determine the
placement in the hierarchy.



A reference item is simply a target Menu Item HTML element that
already exists in the Menu. Any valid jQuery selector can be used to
obtain a reference to the target item. For examples, see the
[Menu API demos](../menu/api.html "Menu API demos").
Removing an item only requires a reference to the target element that
should be removed.

### Dynamically add a new root Menu item

    var menu = $("#menu").kendoMenu().data("kendoMenu");
    menu.insertAfter(
        { text: "New Menu Item" },
        menu.element.children("li:last")
    );

## Accessing an Existing Menu


You can reference an existing **Menu** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the API to control
its behavior.

### Accessing an existing Menu instance

    var menu = $("#menu").data("kendoMenu");

