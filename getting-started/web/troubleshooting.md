---
title: Troubleshooting
slug: widget-troubleshooting
publish: true
---

# Troubleshooting

This page provides solutions for commonly problems you may encounter when working with Kendo UI widgets.

### Problem: The widget object is undefined after loading a page through AJAX

**Cause:** Usually caused when the page loaded via AJAX contains a script reference to jQuery. When jQuery is re-initialized, all jQuery-based data attributes are cleared, including the data("kendoWidget") attribute that holds the Kendo UI widget object.

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
