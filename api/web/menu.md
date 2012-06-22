---
title: kendo.ui.Menu
tags: api,web
publish: true
---

# kendo.ui.Menu

## Description



 The **Menu** displays hierarchical data as a multi-level menu. It provides rich styling for unordered lists
 of items, and can be used for both navigation and executing JavaScript commands. Items can be defined and
 initialized from HTML, or the API can be used to add and remove items.


### Getting Started

#### Create a HTML hierarchical list of items

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

#### Initialize a Menu using a selector within $(document).ready()

    $(document).ready(function() {
        $("#menu").kendoMenu();
    });

#### Initialize the Menu using JSON data object

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

### Customizing Menu Animations


 By default, the **Menu** uses a slide animation to expand and
 reveal sub-items as the mouse hovers. Animations can be easily
 customized using configuration properties, changing the animation
 style and delay. Menu items can also be configured to open on click
 instead of on hover.

#### Changing Menu animation and open behavior

    $("#menu").kendoMenu({
     animation: {
      open: { effects: "fadeIn" },
      hoverDelay: 500
     },
     openOnClick: true
    });

### Dynamically configuring Menu items


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

#### Dynamically add a new root Menu item

    var menu = $("#menu").kendoMenu().data("kendoMenu");
    menu.insertAfter(
     { text: "New Menu Item" },
     menu.element.children("li:last")
    );

### Accessing an Existing Menu


 You can reference an existing **Menu** instance via
 [jQuery.data()](http://api.jquery.com/jQuery.data/).
 Once a reference has been established, you can use the API to control
 its behavior.

#### Accessing an existing Menu instance

    var menu = $("#menu").data("kendoMenu");

## Configuration

### `animation` : **Object** 

A collection of **Animation** objects, used to change default animations. A value of false will disable all animations in the widget.


Available animations for the **Menu** are listed below.  Each animation has a reverse options which is used for the **close** effect by default, but can be over-ridden
by setting the **close** animation.  Each animation also has a direction which can be set off the animation (i.e. **slideIn:Down**).

<div class="details-list">
<dl>
    <dt>**slideIn**</dt>
    <dd>Menu content slides in from the top</dd>
    <dt>**fadeIn**</dt>
    <dd>Menu content fades in</dd>
    <dt>**expand**</dt>
    <dd>Menu content expands from the top down. Similar to slideIn.</dd>
</dl>
</div>

#### Example

    $("#menu").kendoMenu({
         animation: { open: { effects: "fadeIn" } }
     });

### `animation.close` : **Animation** 

The animation that will be used when closing sub menus.

### `animation.open` : **Animation** 

The animation that will be used when opening sub menus.

### `closeOnClick` : **Boolean** *(default: true)*

 Specifies that sub menus should close after item selection (provided they won't navigate).

#### Example

    $("#menu").kendoMenu({
         closeOnClick: false
     });

### `direction` : **String** *(default: "default")*

 Specifies Menu opening direction. Can be "top", "bottom", "left", "right".
You can also specify different direction for root and sub menu items, separating them with space. The example below will initialize the root menu to open upwards and
its sub menus to the left.

#### Example

    $("#menu").kendoMenu({
        direction: "top left"
    });

### `hoverDelay` : **Number** *(default: 100)*

 Specifies the delay in ms before the menu is opened/closed - used to avoid accidental closure on leaving.

#### Example

    $("#menu").kendoMenu({
         hoverDelay: 200
     });

### `openOnClick` : **Boolean** *(default: false)*

 Specifies that the root sub menus will be opened on item click.

#### Example

    $("#menu").kendoMenu({
         openOnClick: true
     });

### `orientation` : **String** *(default: "horizontal")*

 Root menu orientation. Could be horizontal or vertical.

#### Example

    $("#menu").kendoMenu({
         orientation: "vertical"
     });

### `popupCollision` : **String** 

Specifies how Menu should adjust to screen boundaries. By default the strategy is **"fit"** for a sub menu with a horizontal parent,
meaning it will move to fit in screen boundaries in all directions, and **"fit flip"** for a sub menu with vertical parent, meaning it will fit vertically and flip over
its parent horizontally. You can also switch off the screen boundary detection completely if you set the **popupCollision** to false.

#### Example

    $("#menu").kendoMenu({
        popupCollision: false
    });

## Methods

### append

Appends an item to a **Menu** in the specified referenceItem's sub menu.

#### Example

    // get a reference to the menu widget
    var menu = $("#menu").data("kendoMenu");
    //
    menu.append(
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
        }],
        referenceItem
    );

#### Parameters

##### item `Selector`

Target item, specified as a JSON object. Can also handle an array of such objects.

##### referenceItem `Item`

A reference item to append the new item in.

#### Returns

`Menu` Returns the Menu object to support chaining.

### close

Closes a sub-menu of a specified item(s) in a **Menu**.

#### Example

    // get a reference to the menu widget
    var menu = $("#menu").data("kendoMenu");
    // close the sub menu of "Item1"
    menu.close("#Item1");

#### Parameters

##### element `Selector`

Target item selector.

#### Returns

`Menu` Returns the Menu object to support chaining.

### enable

Enables or disables an item of a **Menu**. This can optionally be accomplished on
initialization by setting the **disabled="disabled"** on the desired menu item html element.

#### Example

    // get a reference to the menu widget
    var menu = $("#menu").data("kendoMenu");
    // disable the li menu item with the id "secondItem"
    menu.enable("#secondItem", false);

#### Parameters

##### element `Selector`

Target element

##### enable `Boolean`

Desired state

#### Returns

`Menu` Returns the Menu object to support chaining.

### insertAfter

Inserts an item into a **Menu** after the specified referenceItem.

#### Example

    // get a reference to the menu widget
    var menu = $("#menu").data("kendoMenu");
    //
    menu.insertAfter(
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
        }],
        referenceItem
    );

#### Parameters

##### item `Selector`

Target item, specified as a JSON object. Can also handle an array of such objects.

##### referenceItem `Selector`

A reference item to insert the new item after.

#### Returns

`Menu` Returns the Menu object to support chaining.

### insertBefore

Inserts an item into a **Menu** before the specified referenceItem.

#### Example

    // get a reference to the menu widget
    var menu = $("#menu").data("kendoMenu");
    //
    menu.insertBefore(
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
        }],
        referenceItem
    );

#### Parameters

##### item `Selector`

Target item, specified as a JSON object. Can also handle an array of such objects.

##### referenceItem `Selector`

A reference item to insert the new item before

#### Returns

`Menu` Returns the Menu object to support chaining.

### open

Opens a sub-menu of a specified item(s) in a **Menu**.

#### Example

    // get a reference to the menu widget
    var menu = $("#menu").data("kendoMenu");
    // open the sub menu of "Item1"
    menu.open("#Item1");

#### Parameters

##### element `Selector`

Target item selector.

#### Returns

`Menu` Returns the Menu object to support chaining.

### remove

Removes a specified item(s) from a **Menu**.

#### Example

    // get a reference to the menu widget
    var menu = $("#menu").data("kendoMenu");
    // remove the item with the id "Item1"
    menu.remove("#Item1");

#### Parameters

##### element `Selector`

Target item selector.

#### Returns

`Menu` Returns the Menu object to support chaining.

## Events

### close

Fires after a sub menu gets closed.

#### Example

     $("#menu").kendoMenu({
         close: function(e) {
             // handle event
         }
     });

#### To set after initialization

     // get a reference to the menu widget
     var menu = $("#menu").data("kendoMenu");
     // bind to the close event
     menu.bind("close", function(e) {
         // handle event
     });

#### Event Data

##### e.item `Element`

The closed item

### open

Fires before a sub menu gets opened.

#### Example

     $("#menu").kendoMenu({
         open: function(e) {
             // handle event
         }
     });

#### To set after initialization

     // get a reference to the menu widget
     var menu = $("#menu").data("kendoMenu");
     // bind to the open event
     menu.bind("open", function(e) {
         // handle event
     });

#### Event Data

##### e.item `Element`

The opened item

### select

Fires when a menu item gets selected.

#### Example

     $("#menu").kendoMenu({
         select: function(e) {
             // handle event
         }
     });

#### To set after initialization

     // get a reference to the menu widget
     var menu = $("#menu").data("kendoMenu");
     // bind to the select event
     menu.bind("select", function(e) {
         // handle event
     });

#### Event Data

##### e.item `Element`

The selected item