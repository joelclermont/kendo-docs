---
title: Splitter Overview
slug: splitter-overview
tags: getting-started,web
publish: true
---

# Splitter Overview

The **Splitter** provides a dynamic layout of resizable and collapsible panes. It converts the
children of an HTML element in to the interactive layout, adding resize and collapse handles based on
configuration. A **Splitter** can be mixed in a vertical or horizontal orientation to build
complex layouts.


## Getting Started

The layout and structure of a **Splitter** is defined within the DOM as a div with child elements.

### Create a div with children that will become panes

    <div id="splitter">
        <div>Area 1</div>
        <div>Area 2</div>
    </div>

Initialization of a **Splitter** should occur after the DOM is fully loaded. It is recommended
that initialization the **Splitter** occur within a handler is provided to $(document).ready().

### Initialize the Splitter using a selector within $(document).ready()

    $(document).ready(function() {
        $("#splitter").kendoSplitter();
    });

When the **Splitter** is initialized, a vertical split bar will be placed between the two div
elements. This bar can be moved by a user left and right to adjust the size on the panes.


## Configuring Splitter Behaviors

The **Splitter** has a default configuration specified during initialization. However, these
options may be overriden to control the following properties:


*   Maximum and/or minimum pane sizes
*   Resizable and collapsible/expandable pane behaviors
*   Orientation (horizontal or vertical)



The properties of a pane must be set during initialization and set for each individual pane in a
**Splitter**.

### Initialize a Splitter and the properties of its panes

    $("#splitter").kendoSplitter({
        panes: [
            { collapsible: true, min: "100px", max: "300px" },
            { collapsible: true }
        ],
        orientation: "vertical"
    });


## Nested Splitter Layouts

To achieve complex layouts, the **Splitter** supports nested layouts.

### Creating nested Splitter layout

    <div id="horizontalSplitter">
        <div><p>Left Side Pane Content</p></div>
        <div>
            <div id="verticalSplitter">
                <div><p>Right Side, Top Pane Content</p></div>
                <div><p>Right Side, Bottom Pane Content</p></div>
            </div>
        </div>
    </div>

### Initialize two Splitters with differing orientations

    $("horizontalSplitter").kendoSplitter();
    $("verticalSplitter").kendoSplitter({ orientation: "vertical" });

## Loading Content with AJAX


While any valid technique for loading content via AJAX may be used, **Splitter** provides built-in
support for asynchronously loading content from URLs. These URLs should return HTML fragments that can be
loaded in the pane of a **Splitter**. If you want to load a whole page in an IFRAME, you may do so
by specifying the complete URL (i.e. http://kendoui.com/).

### Loading Splitter content asynchronously

    <div id="splitter">
        <div>Area 1 with Static Content</div>
        <div></div>
        <div></div>
    </div>

### Initialize Splitter; configure async loading for one pane; and an iframe for a third pane

    $(document).ready(function() {
        $("#splitter").kendoSplitter({
            panes: [
                {},
                { contentUrl: "html-content-snippet.html" },
                { contentUrl: "http://kendoui.com/" }
            ]
        });
    });

## Accessing an Existing Splitter

You can reference an existing **Splitter** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

### Accessing an existing Splitter instance

    var splitter = $("#splitter").data("kendoSplitter");

