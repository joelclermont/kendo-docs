---
title: Window Overview
slug: window-overview
tags: getting-started,web
publish: true
---

# Window Overview

A **Window** displays content in a modal or non-modal HTML window. By default, a
**Window** can be moved, resized, and closed. Its content can also be defined with either as
static HTML or loaded dynamically via AJAX.

A **Window** can be initialized from virtually any DOM element. During initialization, the
targeted content will automatically be wrapped in the div element of the **Window**.


## Getting Started

### Create a simple HTML element with the Window content

    <div id="window">
        Content of the Window
    </div>

### Initialize the Window using a selector

    $(document).ready(function() {
        $("#window").kendoWindow();
    });

When a **Window** is initialized, it will automatically be displayed open near the location of the
DOM element that was used to initialize the content.


## Configuring Window Behaviors


A **Window** provides many configuration options that can be easily set during initialization.
Among the properties that can be controlled:


*   Minimum height/width
*   Available user actions (close/refresh/maximize/minimize) and ability to define custom ones
*   Title
*   Draggable and resizable behaviors

### Create a modal Window with all user actions enabled

    $("#window").kendoWindow({
        actions: ["Custom", "Refresh", "Maximize", "Minimize", "Close"],
        draggable: false,
        height: "300px",
        modal: true,
        resizable: false,
        title: "Modal Window",
        width: "500px"
    });

The order of the values in the actions array determines the order in which the action buttons will be rendered
in the title of a **Window**. The maximize action serves both as a button for expanding a
**Window** to fill the screen and as a button to restore a **Window** to its previous
size. The minimize action collapses a **Window** to its title.


If a non-recognized action name is supplied, it is treated as a custom action - **k-icon** and **k-actionname**
CSS classes are rendered for it and no click event handler is attached automatically. The Kendo stylesheets have a supplied icon for
actions with the name "Custom", but any name can be used. Click events can be captured and handled in a standard way:

### Custom actions

      $("#window").kendoWindow({
          actions: ["Custom", "Minimize", "Maximize", "Close"],
          title: "Window Title"
      }).data("kendoWindow").wrapper.find(".k-i-custom").click(function(e) {
          alert("Custom action button clicked");
          e.preventDefault();
      });

    <h3>Positioning and Opening a Window</h3>
    <p>
     In some scenarios, it is preferable to center a <strong>Window</strong> rather than open it near the HTML
     element used to define the content. It is also common to open a <strong>Window</strong> as the result of the
     action of a user rather than on the load event of a page. The <strong>Window</strong> API provides methods for
     handling these scenarios.
    </p>

### Centering a Window and opening on button click

    <div id="window">
        Content of the Window
    </div>
    <button id="openButton">Open Window</button>

### Initialize Window, center, and configure button click action

    $(document).ready(function(){
        var win = $("#window").kendoWindow({
            height: "200px",
            title: "Centered Window",
            visible: false,
            width: "200px"
        }).data("kendoWindow");
    });

    $("#openButton").click(function(){
        var win = $("#window").data("kendoWindow");
        win.center();
        win.open();
    });

## Loading Window content via AJAX


A **Window** provides built-in support for asynchronously loading content from a URL. This URL
should return a HTML fragment that can be loaded in a Window content area.

### Load Window content asynchronously

    <div id="window"></div>

### Initialize window and configure content loading

    $(document).ready(function(){
        $("#window").kendoWindow({
            content: "html-content-snippet.html",
            title: "Async Window Content"
        });
    });

## Accessing an Existing Window


You can reference an existing **Window** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

### Accessing an existing Window instance

    var win = $("#window").data("kendoWindow");


