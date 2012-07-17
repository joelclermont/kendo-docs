---
title: PanelBar Overview
slug: gs-web-panelbar-overview
tags: getting-started,web
publish: true
---

# PanelBar Overview

The **PanelBar** displays hierarchical data as a multi-level, expandable widget that is useful for
constrained areas of a page. Its structure may be defined in HTML or configured dynamically through its API. The
content for items can also be loaded via AJAX by specifying a content URL.


## Getting Started

A **PanelBar** can be created by targeting the root element of a HTML list. A
**PanelBar** will utilize this list to define its structure and content.

### Create a list of items

    <ul id="panelBar">
        <li>
            Item 1
                <ul>
                    <li>Sub Item 1</li>
                    <li>Sub Item 2</li>
                </ul>
        <li>
        <li>Item 2</li>
    </ul>

Initialization of a **PanelBar** should occur after the DOM is fully loaded. It is recommended
that initialization the **PanelBar** occur within a handler is provided to $(document).ready().

### Initialize the PanelBar via an ID selector

    $(document).ready(function() {
        $("#panelBar").kendoPanelBar();
    });

**PanelBar** items may contain nested content (including markup) within a **div**
element. Text content located outside nested content will be used as the title of the item.

### Create a list of items in HTML with nested content

    <ul id="panelBar">
        <li>Item with no content</li>
        <li>Item with content
            <div>This is nested content of a PanelBar item.</div>
        </li>
    </ul>

A **PanelBar** will preserve the content defined within an item.

### Initialize the PanelBar via an ID selector

    var panelBar = $("#panelbar").kendoPanelBar();

### Initialize a PanelBar using JSON data object

    $("#panelbar").kendoPanelBar({
        dataSource: [
            {
                text: "Item 1",
                url: "http://www.kendoui.com/"                  // link URL if navigation is needed (optional)
            },
            {
                text: "<b>Item 2</b>",
                encoded: false,                                 // Allows use of HTML for item text
                content: "text"                                 // content within an item
            },
            {
                text: "Item 3",
                contentUrl: "partialContent.html"               // content URL to load within an item
            },
            {
                text: "Item 4",
                imageUrl: "http://www.kendoui.com/test.jpg",    // item image URL, optional
                expanded: true,                                 // item is rendered expanded
                items: [{                                       // Sub item collection.
                    text: "Sub Item 1"
                },
                {
                    text: "Sub Item 2"
                }]
            },
            {
                text: "Item 5",
                // item image sprite CSS class, optional
                spriteCssClass: "imageClass3"
            }
        ]
    });

## Loading Content with AJAX


While any valid technique for loading AJAX content can be used, the **PanelBar** provides built-in
support for asynchronously loading content from URLs. These URLs should return HTML fragments that can be
loaded in the **PanelBar** item content area. Content DIVs should be completely empty for AJAX
loading to work.

### Create a list of items with a target for dynamic content

    <ul id="panelBar">
        <li>Item 1
            <ul>
                <li>Sub Item 1</li>
            </ul>
        </li>
        <li>Item 2</li>
        <li>
            Item with Dynamic Content
            <div></div>
        </li>
    </ul>

### Load a PanelBar item content asynchronously via AJAX

    $("#panelBar").kendoPanelBar({
        contentUrls:[
            null,
            null,
            "html-content-snippet.html"
        ]
    });

When the **PanelBar** loads remote content via AJAX, the server response is cached in-memory so
that subsequent expand/collapse actions do not trigger subsequent AJAX requests.


## Customizing PanelBar Animations


By default, a **PanelBar** uses animations to expand and reveal sub-items when an item header is
clicked. These animations can be modified in configuration via the open and close animation properties. A
**PanelBar** can also be configured to only allow one panel to remain open at a time.

### Changing PanelBar animation and expandMode behavior

    $("#panelBar").kendoPanelBar({
        animation: {
            open : { effects: "fadeIn" }
        },
        expandMode: "single"
    });

## Dynamically Configuring PanelBar Items


The **PanelBar** API provides several methods for dynamically adding or removing Items. To add
items, provide the new item as a JSON object along with a reference item that will be used to determine its
placement in the items hierarchy. Note: The reference item is optional when appending.



A reference item is a target **PanelBar** item HTML element that already exists in the PanelBar.
Any valid selector can be used to obtain a reference to the target item.


Removing an item only requires a reference to the target element that should be removed.

### Dynamically adding a new root PanelBar item

    var panelBar = $("#panelBar").kendoPanelBar().data("kendoPanelBar");

    panelBar.insertAfter(
         { text: "New PanelBar Item" },
         panelBar.element.children("li:last")
    );

## Accessing an Existing PanelBar


You can reference an existing **PanelBar** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

### Accessing an existing PanelBar instance

    var panelBar = $("#panelBar").data("kendoPanelBar");

