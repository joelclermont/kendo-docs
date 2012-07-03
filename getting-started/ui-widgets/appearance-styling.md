---
title: Appearance and Styling
slug: widget-appearance-and-styling
publish: true
---

<style>
.content-main .prettyprint { overflow-x: auto; }
</style>
The appearance of the** Kendo UI** widgets depends entirely on styles defined by the applied CSS classes. No inline styles are used, except for some very specific cases when they must be set with Javascript, depending on the browser or configuration.

### Common and Skin StyleSheets
 **Kendo UI** always uses a pair of stylesheets -** kendo.common.css** and **kendo.[skin].css**. The common (base) stylesheet applies styles related to positioning and size, which are not related to the color scheme and are always required for the widget to look (and work) properly. The skin stylesheet applies styles related to colors and backgrounds, which are skin-specific.

Be sure to include the common CSS file before the skin CSS file, because in some cases the skin CSS file may override base styles because it uses selectors with the same specificity.

### Primitives

The widgets use the so-called primitives, i.e. different HTML elements in different widgets use the same CSS classes to provide a level of abstraction and allow common styling.

Here is an outline of the CSS classes that are commonly used.

*   **k-widget** - applied to the widget wrapper to set a border, text and background color. In addition to t-widget, every widget has its own specific CSS class, for example **k-menu**, **k-panelbar**, **k-tabstrip**, etc.
*   **k-header** - applied to Grid headers, Menu top level items, PanelBar top level items, TabStrip items, DropDownLists, to set a background image and a background color
*   **k-link** - applied to hyperlinks and clickable text items to set a text color
*   **k-button** - applied to elements that should look like push buttons. The class sets a text color, background color, background image and hover styling. This is the **recommended **class for styling **form buttons**
*   **k-input** - applied to textboxes inside input widgets like ComboBox and AutoComplete to set border, text and background color
*   **k-textbox** - same as k-input, but used for standalone (generic) input elements that are not part of widget. This is the **recommended **class for styling user** form input elements** as it provides the same look, height and vertical alignment as the Kendo UI input widgets
*   **k-group** and **k-content** - applied to various containers to set a background and border color
*   **k-popup** - applied to popup containers that are detached from their opener component and are placed in the &lt;body&gt; element
*   **k-icon** and **k-sprite** - applied to elements that display part of a sprite image as background to init their dimensions
*   **k-image** - applied to inline images to set their dimensions*   **k-item** - applied to various repeating widget items, e.g. in the Menu, TabStrip, TreeView, PanelBar, ComboBox, DropDownList, etc. This CSS class does not apply any particular global styles and sports display: block.
*   **k-first** and **k-last** - set on first and last k-item respectively, where special styling is needed - rounded corners, removing borders 

The appearance of a component or part of it may depend on its state, which is tied to a CSS class as well:

*   **k-state-default** - this class is applied on items to set their default appearance background and colors
*   **k-state-hover** - this class is set to items when they are hovered to apply their hovered look
*   **k-state-focused** - this class is applied on focused mostly input elements (plus DropDownList)
*   **k-state-active** - a class set on activated **k-link** elements
*   **k-state-selected** - selected items receive this class to apply their selected look, like in PanelBar and TabStrip
*   **k-state-disabled** - this class is set on disabled items 

### Customizing Appearance

Usually, a CSS property defined by a primitive CSS class is used by all widgets that use this CSS class, unless overridden by a higher specificity selector. For example:
  
    .k-link
    {
    color: blue;
    }
      

will not affect
  
    .k-panelbar .k-link
    {
    color: red;
    }
      

because its specificity is 10 and the latter is 20\. For more information about specificity, check [this excellent article in Smashing Magazine](http://www.smashingmagazine.com/2007/07/27/css-specificity-things-you-should-know/).

If you want to override the styling of a particular widget, you can use a CSS selector with the widget's own CSS class:
  
    .k-menu .k-link
    {
    color: red;
    }
      

Though, make sure that you specify it after the inclusion of the respective skin CSS files.