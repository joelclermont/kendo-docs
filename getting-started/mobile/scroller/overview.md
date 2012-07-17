---
title: Mobile Scroller Overview
slug: gs-mobile-scroller
tags: getting-started,mobile
publish: true
---

# Mobile Scroller Overview

The Kendo Mobile Scroller widget enables touch friendly kinetic scrolling for the contents of a given DOM element.

## Getting Started

Each mobile View initializes a scroller for its content element. In addition to that, a scroller will be initialized for every element with a
`role` data attribute set to `scroller`.
Alternatively, it can be initialized using jQuery plugin syntax in the containing mobile View **init event handler**.


For the scroller to work, its element should have fixed dimensions (width and/or height) set.

### Initialize mobile Scroller using a role data attribute.

    <div data-role="scroller">
        Foo
    </div>

### Initialize mobile Scroller using jQuery plugin syntax

    <div id="scroller"></div>

    <script>
        var scroller = $("#scroller").kendoMobileScroller();
    </script>

### Obtain the current mobile view scroller

    <div data-role="view" data-init="getScroller">
        Foo
    </div>

    <script>
        function getScroller(e) {
            var scroller = e.view.scroller;
        }
    </script>

The mobile Scroller widget exposes the following fields:

*   **scrollTop** - the number of pixels that are hidden from view above the scrollable area.
*   **scrollLeft** - the number of pixels that are hidden from view to the left of the scrollable area.

