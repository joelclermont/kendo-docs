---
title: kendo.ui.TabStrip
slug: web-kendo.ui.tabstrip
tags: api,web
publish: true
---

# kendo.ui.TabStrip

## Configuration

### animation `Object`

A collection of visual animations used when **TabStrip** tab are selected through
user interactions. Setting this option to **false** will disable all animations.

#### Example

    $("#tabstrip").kendoTabStrip({
        animation: {
            // fade-out current tab over 1000 milliseconds
            close: {
                duration: 1000,
                effects: "fadeOut"
            },
           // fade-in new tab over 500 milliseconds
           open: {
               duration: 500,
               effects: "fadeIn"
           }
       }
    });

### animation.close `Object`

The visual animation(s) that will be used when the current tab is closed.

#### Example

    $("#tabstrip").kendoTabStrip({
        animation: {
            close: {
                duration: 200,
                effects: "fadeOut"
            }
        }
    });

### animation.close.duration `Number`*(default: 200)*

The number of milliseconds used for the visual animation when the current tab is closed.

#### Example

    $("#tabstrip").kendoTabStrip({
        animation: {
            close: {
    
                       duration: 1000
    
                   }
      }
    });

### animation.close.effects `String`

A whitespace-delimited string of animation effects that are utilized when the current tab
is closed. By default not specified - uses the opening animation with reverse.

#### Example

    $("#tabstrip").kendoTabStrip({
        animation: {
            close: {
                duration: 1000,
                effects: "fadeOut"
            }
        }
    });

### animation.open `Object`

The visual animation(s) that will be used when the new tab is shown.

#### Example

    $("#tabstrip").kendoTabStrip({
        animation: {
            open: {
                duration: 200,
                effects: "expand:vertical"
            }
        }
    });

### animation.open.duration `Number`*(default: 200)*

The number of milliseconds used for the visual animation when a new tab is shown.

#### Example

    $("#tabstrip").kendoTabStrip({
     animation: {
          open: {
              duration: 1000
          }
       }
    });

### animation.open.effects `String`*(default: "expand:vertical fadeIn")*

A whitespace-separated string of animation effects that are used when a new tab is shown. Options include
**"expand:vertical"** and **"fadeIn"**.

### animation.open.show `Boolean`*(default: true)*



### collapsible `Boolean`*(default: false)*

Specifies whether the TabStrip should be able to collapse completely when clicking an expanded tab.

#### Example

    $("#tabstrip").kendoTabStrip({
        collapsible: true
    });

### dataContentField `String`*(default: "")*

 Sets the field of the data item that provides the text content of
the tab content element.

#### Example

    $("#tabstrip").kendoTabStrip({
        dataTextField: "Name",
        dataContentField: "Content",
        dataSource: data
    });

### dataContentUrlField `String`*(default: "")*

 Sets the field of the data item that provides the URL for
the ajax loaded tab content.

#### Example

    $("#tabstrip").kendoTabStrip({
        dataTextField: "Name",
        dataContentUrlField: "ContentUrl",
        dataSource: data
    });

### dataImageUrlField `String`*(default: "")*

 Sets the field of the data item that provides the image URL of
the tab.

#### Example

    $("#tabstrip").kendoTabStrip({
        dataTextField: "Name",
        dataImageUrlField: "ImageUrl",
        dataSource: data
    });

### dataSpriteCssClass `String`*(default: "")*

 Sets the field of the data item that provides the CSS class of
the tab.

#### Example

    $("#tabstrip").kendoTabStrip({
        dataTextField: "Name",
        dataSpriteCssClass: "CssClass",
        dataSource: data
    });

### dataTextField `String`*(default: "")*

 Sets the field of the data item that provides the text name of the tab.

#### Example

    $("#tabstrip").kendoTabStrip({
        dataTextField: "Name",
        dataSource: data
    });

### dataUrlField `String`*(default: "")*

 Sets the field of the data item that provides the link URL for the
tab.

#### Example

    $("#tabstrip").kendoTabStrip({
        dataTextField: "Name",
        dataUrlField: "Url",
        dataSource: data
    });

## Methods

### activateTab

Activates a tab specified as a selector. Note: Invoking this method will not trigger any events.

#### Activate a tab with ID, tab1 in a TabStrip

    var tabToActivate = $("#tab1");
    $("#tabStrip").data("kendoTabStrip").activateTab(tabToActivate);

#### Parameters

##### item `Selector`

The target tab, specified as a selector, to be activated.

#### Returns

`Boolean` Returns <strong>true</strong> if successful; otherwise, <strong>false</strong>.

### append

Appends a tab to the collection of tabs in a **TabStrip**.

#### Example

    tabStrip.append(
        [{
            text: "Item 1",
            url: "http://www.kendoui.com"               // Link URL if navigation is needed, optional.
        },
        {
            text: "<b>Item 2</b>",
            encoded: false,                             // Allows use of HTML for item text
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
    );

#### Parameters

##### tab `Selector`

Target tab, specified as a JSON object. You can pass tab text, content or contentUrl here. Can handle an
HTML string or array of such strings or JSON.

#### Returns

`TabStrip` Returns the TabStrip object to support chaining.

### contentElement

Obtains the DOM element representing a tab by its index in the **TabStrip**.

#### Obtain the DOM element representing the first tab in a TabStrip

    var tabContent = $("#tabStrip").data("kendoTabStrip").contentElement(0);

#### Parameters

##### itemIndex `int`

The index of the tab in the TabStrip.

#### Returns

`HTMLElement` The DOM element representing a tab by its index in the <strong>TabStrip</strong>.

### deactivateTab

Deactivates a tab specified as a selector. Note: Invoking this method will not trigger any events.

#### Example

    var tabToDeactivate = $("#tab1");
    $("#tabStrip").data("kendoTabStrip").deactivateTab(tabToActivate);

#### Parameters

##### item `Selector`

The target tab, specified as a selector, to be deactivated.

### disable

Disables a tab(s) of a **TabStrip**.

#### Parameters

##### element `Selector`

The target tab(s), specified as a selector, to be disabled.

#### Returns

`TabStrip` Returns the TabStrip object to support chaining.

### enable

Disables (**false**) or enables (**true**) a tab(s) of a **TabStrip**.

#### Parameters

##### element `Selector`

The target tab(s), specified as a selector, to be enabled (**true**) or disabled
(**false**).

##### enable `Boolean`

Desired state of the tab(s) specified by the selector; enabled (**true**) or disabled
(**false**).

#### Returns

`TabStrip` Returns the TabStrip object to support chaining.

### insertAfter

Inserts a newly-created tab after a specified tab.

#### Example

    tabStrip.insertAfter(
        [{
            text: "Item 1",
            url: "http://www.kendoui.com"               // Link URL if navigation is needed, optional.
        },
        {
            text: "<b>Item 2</b>",
            encoded: false,                             // Allows use of HTML for item text
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
        }],
        referenceItem
    );

#### Parameters

##### item `Selector`

Target tab, specified as a JSON object. You can pass tab text, content or contentUrl here. Can handle an
HTML string or array of such strings or JSON.

##### referenceTab `Item`

A reference tab to insert the new item after.

#### Returns

`TabStrip` Returns the TabStrip object to support chaining.

### insertBefore

Inserts a newly-created tab before a specified tab.

#### Example

    tabStrip.insertBefore(
        [{
            text: "Item 1",
            url: "http://www.kendoui.com"               // Link URL if navigation is needed, optional.
        },
        {
            text: "<b>Item 2</b>",
            encoded: false,                             // Allows use of HTML for item text
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
        }],
        referenceItem
    );

#### Parameters

##### item `Selector`

Target tab, specified as a JSON object. You can pass tab text, content or contentUrl here. Can handle an
HTML string or array of such strings or JSON.

##### referenceTab `Item`

A reference tab to insert the new item before

#### Returns

`TabStrip` Returns the TabStrip object to support chaining.

### reload

Reloads TabStrip tab(s) via AJAX.

#### Parameters

##### element `Selector`

The target tab(s), specified as a selector, to be reloaded via AJAX.

#### Returns

`TabStrip` Returns the TabStrip object to support chaining.

### remove

Removes a specified tab from a TabStrip.

#### Remove a tab with ID, tab1 from a TabStrip

    tabStrip.remove("#tab1");

#### Parameters

##### element `Selector`

The target tab(s), specified as a selector, to be removed.

#### Returns

`TabStrip` Returns the TabStrip object to support chaining.

### select

Selects the specified tab(s) within a **TabStrip**. If called without arguments, it returns the
currently selected tab.

#### Example

    tabStrip.select("#tab1");

#### Example

    tabStrip.select(1);

#### Parameters

##### element `Selector/Index`

or index
The target tab(s), specified as a selector or index in the tab group.

#### Returns

`TabStrip` Returns the TabStrip object to support chaining.

## Events

### activate

Triggered just after a tab is being made visible, but before the end of the animation

#### Attach activate event handler during initialization; detach via unbind()

    // event handler for activate
    var onActivate = function(e) {
        // access the activated item via e.item (HTMLElement)
    };
    
    // attach activate event handler during initialization
    var tabStrip = $("#tabStrip").kendoTabStrip({
        activate: onActivate
    });
    
    // detach activate event handler via unbind()
    tabStrip.data("kendoTabStrip").unbind("activate", onActivate);

#### Attach activate event handler via bind(); detach via unbind()

    // event handler for activate
    var onActivate = function(e) {
        // access the activated item via e.item (HTMLElement)
    };
    
    // attach activate event handler via bind()
    $("#tabStrip").data("kendoTabStrip").bind("activate", onActivate);
    
    // detach activate event handler via unbind()
    $("#tabStrip").data("kendoTabStrip").unbind("activate", onActivate);

#### Event Data

##### e.item `HTMLElement`

The activated tab.

##### e.contentElement `Element`

The content element of the activated tab.

### contentLoad

Triggered when content is fetched from an AJAX request.

#### Event Data

##### e.item `Element`

The selected item

##### e.contentElement `Element`

The loaded content element that is retrieved via AJAX.

### error

Triggered when an AJAX request results in an error.

#### Event Data

##### e.xhr `jqXHR`

The jqXHR object used to load the content

##### e.status `String`

The returned status.

### select

Triggered before a tab is selected.

#### Attach select event handler during initialization; detach via unbind()

    // event handler for select
    var onSelect = function(e) {
        // access the selected item via e.item (HTMLElement)
    };
    
    // attach select event handler during initialization
    var tabStrip = $("#tabStrip").kendoTabStrip({
        select: onSelect
    });
    
    // detach select event handler via unbind()
    tabStrip.data("kendoTabStrip").unbind("select", onSelect);

#### Attach select event handler via bind(); detach via unbind()

    // event handler for select
    var onSelect = function(e) {
        // access the selected item via e.item (HTMLElement)
    };
    
    // attach select event handler via bind()
    $("#tabStrip").data("kendoTabStrip").bind("select", onSelect);
    
    // detach select event handler via unbind()
    $("#tabStrip").data("kendoTabStrip").unbind("select", onSelect);

#### Event Data

##### e.item `HTMLElement`

The selected item chosen by a user.

##### e.contentElement `Element`

The content element of the tab going to be selected.
