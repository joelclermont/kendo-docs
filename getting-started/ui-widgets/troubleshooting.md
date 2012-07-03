---
title: Troubleshooting
slug: widget-troubleshooting
publish: true
---

## Troubleshooting

This page suggests solutions for commonly encountered problems with the Kendo UI widgets.

### The widget object is undefined after loading a page through AJAX

**Causation:** Usually caused when the loaded page contains a script reference to jQuery. This causes all jQuery-based data attributes to be cleared, and in particular the data("kendoWidget") that holds the widget object.

**Solution:** Load a partial HTML fragment that doesn't contain any unneeded jQuery references, or use an iframe to load the complete page.

**Example: problem**
  
    $("#dialog").kendoWinodow({
    // loads complete page
    content: "/foo"
    });  

**Example: solution**
  
    $("#dialog").kendoWinodow({
    // load complete page...
    content: "/foo",
    // ... and show it in an iframe
    iframe: true
    }); 
or
 
    $("#dialog").kendoWinodow({
     // load partial page, without jQuery reference
    content: "/foo"
    }); 