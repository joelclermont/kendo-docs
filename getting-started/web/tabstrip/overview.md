---
title: TabStrip Overview
slug: getting-started.web.tabstrip
tags: getting-started,web
publish: true
---

# TabStrip Overview

A **TabStrip** displays a collection of tabs with associated content. It is composed of an
unordered list of items - representing tabs - and a collection of div elements, which contain the content for
each tab.


## Getting Started

### Create an unordered list for tabs with associated div elements for content

    <div id="tabStrip">
        <ul>
            <li>First tab</li>
            <li>Second tab</li>
        </ul>
        <div>First tab content</div>
        <div>Second tab content</div>
    </div>

Initialization of a **TabStrip** should occur after the DOM is fully loaded. It is recommended
that initialization the **TabStrip** occur within a handler is provided to $(document).ready().

### Initialize a TabStrip using a selector within $(document).ready()

    $(document).ready(function() {
        $("#tabStrip").kendoTabStrip();
    });

### Initialize the TabStrip using JSON data object

    $(document).ready(function() {
        $("#tabstrip").kendoTabStrip({
            dataTextField: "text",
            dataContentField: "content",
            dataUrlField: "url",
            dataImageUrlField: "imageUrl",
            dataSpriteCssClass: "spriteCssClass",
            dataContentUrlField: "contentUrl",
            dataSource:
            [{
                text: "Item 1",
                url: "http://www.kendoui.com"               // Link URL if navigation is needed, optional.
            },
            {
                text: "Item 2",
                content: "text"                             // Content for the content element
            },
            {
                text: "Item 3",
                contentUrl: "partialContent.html"           // From where to load the item content
            },
            {
                text: "Item 4",
                imageUrl: "http://www.kendoui.com/test.jpg" // Item image URL, optional.
            },
            {
                text: "Item 5",
                spriteCssClass: "imageClass3"               // Item image sprite CSS class, optional.
            }]
        });
    });

The tabs of a **TabStrip** are not required to have content. Should a tab have no content, it is
safe to omit its associated div.


## Loading TabStrip content with AJAX


While any valid technique for loading AJAX content can be used, a **TabStrip** supports loading
content from URLs in an asynchronous manner. These URLs should return HTML fragments that can be loaded in a
TabStrip content area. Content DIVs are not required and if present should be completely empty for AJAX loading
to work.

### Loading Tab content asynchronously

    <div id="tabstrip">
        <ul>
            <li>First Tab</li>
            <li>Second Tab</li>
        </ul>
        <div></div>
        <div></div>
     </div>

### Initialize TabStrip and configure one tab with async content loading

    $(document).ready(function(){
        $("#tabstrip").kendoTabStrip({
            contentUrls: [null, "html-content-snippet.html"]
        });
     });

## Dynamically Configure TabStrip Tabs


The **TabStrip** API provides several methods for dynamically adding or removing tabs. To add
tabs, provide the new item as a JSON object along with a reference item that will be used to determine the
placement in the **TabStrip**. Note: append() does not require a reference item.

A reference item is simply a target DOM element of a tab that already exists in the TabStrip. Any valid
selector may be used to obtain a reference to the target item.


Removing an item requires a reference to the target element.

### Dynamically add a new tab

    var tabStrip = $("#tabStrip").data("kendoTabStrip");
    tabStrip.insertAfter(
        { text: "New Tab" },
        tabstrip.tabGroup.children("li:last")
    );

## Selecting a Tab on Initial Load


It is possible to select a tab and display its associated content upon its initial load. There are two (2) ways
to accomplish this task:


1.  Add a "k-state-active" class to the DOM element of the tab
2.  Use select() to target and select a tab either by selector or index


Both approaches produce the same result.

### Selecting a default tab manually using HTML

    <div id="tabstrip">
        <ul>
            <li class="k-state-active">First Tab</li>
            <li>Second Tab</li>
        </ul>
        <div></div>
        <div></div>
    </div>

### Initialize a TabStrip and select first tab via select(element)

    $(document).ready(function(){
        var tabstrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        tabstrip.select(tabstrip.tabGroup.children("li:first"));
    });

### Initialize a TabStrip and select first tab via select(index)

    $(document).ready(function(){
        var tabstrip = $("#tabstrip").kendoTabStrip().data("kendoTabStrip");
        tabstrip.select(1);
    });

## Accessing an Existing TabStrip


You can reference an existing **TabStrip** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

### Accessing an existing TabStrip instance

    var tabStrip = $("#tabStrip").data("kendoTabStrip");

