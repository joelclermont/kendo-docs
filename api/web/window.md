---
title: kendo.ui.Window
slug: web-kendo.ui.window
tags: api,web
publish: true
---

# kendo.ui.Window

## Configuration

### actions `Array`*(default: ["Close"])*

The buttons for interacting with the window. Predefined array values are "Close", "Refresh", "Minimize",
and "Maximize".

### animation `Object`

A collection of {Animation} objects, used to change default animations. A value of **false**
will disable all animations in the widget.

### animation.close `Animation`

The animation that will be used when a Window closes.

### animation.open `Animation`

The animation that will be used when a Window opens.

### appendTo `Object`*(default: document.body)*

The element that the Window will be appended to.

### content `Object|String`

Specifies a URL or request options that the window should load its content from. For remote URLs, a
container iframe element is automatically created.

### content.template `String`

Template for the content of a **Window**.

### draggable `Boolean`*(default: true)*

Enables (**true**) or disables (**false**) the ability for users to move/drag a
**Window**.

### iframe `Boolean`

Explicitly states whether content iframe should be created.

### maxHeight `Number`*(default: Infinity)*

The maximum height (in pixels) that may be achieved by resizing the window.

### maxWidth `Number`*(default: Infinity)*

The maximum width (in pixels) that may be achieved by resizing the window.

### minHeight `Number`*(default: 50)*

The minimum height (in pixels) that may be achieved by resizing the window.

### minWidth `Number`*(default: 50)*

The minimum width (in pixels) that may be achieved by resizing the window.

### modal `Boolean`*(default: false)*

Specifies whether the window should show a modal overlay over the page.

### resizable `Boolean`*(default: true)*

Enables (**true**) or disables (**false**) the ability for users to resize a
**Window**.

### title `String`

The text in the window title bar.

### visible `Boolean`*(default: true)*

Specifies whether the window will be initially visible.

## Methods

### center

Centers a **Window** within the viewport.

#### Example

    var kendoWindow = $("#window").data("kendoWindow");
    kendoWindow.center();

#### Returns

`Window` Returns the (Kendo UI) Window object to support chaining.

### close

Closes a Window.

#### Close a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").close();

#### Returns

`Window` Returns the (Kendo UI) Window object to support chaining.

### content

Gets or set the content of a **Window**.

#### Get the existing content of the Window

    var kendoWindow = $("#window").data("kendoWindow");
    var windowContent = kendoWindow.content();

#### Set the title of a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").content("Kendo UI for all the things!");

#### Parameters

##### content `String`

_optional, default: _

The content of the Window.

#### Returns

`Window` If content is provided, this method will return the (Kendo UI) Window object to support chaining. Otherwise,
it will return the current content of the (Kendo UI) Window.

### destroy

Destroys the window and its modal overlay, if necessary. Removes the Window HTML elements from the DOM.

### maximize

Maximizes a Window to the entire viewing area of the user agent. Triggers the resize event.

#### Maximize a Window

    $("#window").data("kendoWindow").maximize();

#### Returns

`Window` Returns the (Kendo UI) Window object to support chaining.

### minimize

Maximizes a Window to its title bar.

#### Minimize a Window

    $("#window").data("kendoWindow").minimize();

#### Returns

`Window` Returns the (Kendo UI) Window object to support chaining.

### open

Opens a Window.

#### Open a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").open();

#### Returns

`Window` Returns the (Kendo UI) Window object to support chaining.

### refresh

Refreshes the content of a Window from a remote URL.

#### Example

    var windowObject = $("#window").data("kendoWindow");
    windowObject.refresh("/feedbackForm");
    
    windowObject.refresh({
        url: "/feedbackForm",
        data: { userId: 42 }
    });
    
    windowObject.refresh({
        url: "/userInfo",
        data: { userId: 42 },
        template: "Hello, #= firstName # #= lastName #"
    });

#### Parameters

##### options `Object|String`

Options for requesting data from the server.
If omitted, the window uses the `content` property
that was supplied when the window was created.
Any options specified here are passed to jQuery.ajax().

##### options.url `String`

The server URL that will be requested.

##### options.data `Object`

A JSON object containing the data that will be passed to the server.

##### options.type `String`

The HTTP request method ("GET", "POST").

##### options.template `String`

A template to be used for displaying the requested data.

#### Returns

`Window` Returns the (Kendo UI) Window object to support chaining.

### restore

Restores a maximized or minimized Window to its previous state. Triggers the resize event.

#### Restore the state of a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").restore();

#### Returns

`Window` Returns the (Kendo UI) Window object to support chaining.

### title

Gets or set the title of a **Window**.

#### Get the existing title of the Window

    var kendoWindow = $("#window").data("kendoWindow");
    var windowTitle = kendoWindow.title();

#### Set the title of a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").title("Do a barrel roll!");

#### Parameters

##### text `String`

_optional, default: _

The title of the Window.

#### Returns

`Window` If a title is provided, this method will return the (Kendo UI) Window object to support chaining. Otherwise,
it will return the current title of the (Kendo UI) Window.

### toFront

Brings forward a Window to the top of the z-index.

#### Bring forward a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").toFront();

#### Returns

`Window` Returns the (Kendo UI) Window object to support chaining.

### toggleMaximization

Toggles a Window between a maximized and restored state. Triggers the resize event.

#### Toggle the state of a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").toggleMaximization();

#### Returns

`Window` Returns the (Kendo UI) Window object to support chaining.

## Events

### activate

Triggered when a Window has finished its opening animation.

#### Attach activate event handler during initialization; detach via unbind()

    // event handler for activate
    var onActivate = function(e) {
        // ...
    };
    
    // attach activate event handler during initialization
    var kendoWindow = $("#window").kendoWindow({
        activate: onActivate
    });
    
    // detach activate event handler via unbind()
    kendoWindow.data("kendoWindow").unbind("activate", onActivate);

#### Attach activate event handler via bind(); detach via unbind()

    // event handler for activate
    var onActivate = function(e) {
        // ...
    };
    
    // attach activate event handler via bind()
    $("#window").data("kendoWindow").bind("activate", onActivate);
    
    // detach activate event handler via unbind()
    $("#window").data("kendoWindow").unbind("activate", onActivate);

### close

Triggered when a Window is closed (by a user or through the close() method).

#### Attach close event handler during initialization; detach via unbind()

    // event handler for close
    var onClose = function(e) {
        // ...
    };
    
    // attach close event handler during initialization
    var kendoWindow = $("#window").kendoWindow({
        close: onClose
    });
    
    // detach close event handler via unbind()
    kendoWindow.data("kendoWindow").unbind("close", onClose);

#### Attach close event handler via bind(); detach via unbind()

    // event handler for close
    var onClose = function(e) {
        // ...
    };
    
    // attach close event handler via bind()
    $("#window").data("kendoWindow").bind("close", onClose);
    
    // detach close event handler via unbind()
    $("#window").data("kendoWindow").unbind("close", onClose);

### deactivate

Triggered when a Window has finished its closing animation.

#### Attach deactivate event handler during initialization; detach via unbind()

    // event handler for deactivate
    var onDeactivate = function(e) {
        // ...
    };
    
    // attach deactivate event handler during initialization
    var kendoWindow = $("#window").kendoWindow({
        deactivate: onDeactivate
    });
    
    // detach deactivate event handler via unbind()
    kendoWindow.data("kendoWindow").unbind("deactivate", onDeactivate);

#### Attach deactivate event handler via bind(); detach via unbind()

    // event handler for deactivate
    var onDeactivate = function(e) {
        // ...
    };
    
    // attach deactivate event handler via bind()
    $("#window").data("kendoWindow").bind("deactivate", onDeactivate);
    
    // detach deactivate event handler via unbind()
    $("#window").data("kendoWindow").unbind("deactivate", onDeactivate);

### dragend

Triggered when a Window has been moved by a user.

#### Attach dragEnd event handler during initialization; detach via unbind()

    // event handler for dragEnd
    var onDragEnd = function(e) {
        // ...
    };
    
    // attach dragEnd event handler during initialization
    var kendoWindow = $("#window").kendoWindow({
        dragend: onDragEnd
    });
    
    // detach dragEnd event handler via unbind()
    kendoWindow.data("kendoWindow").unbind("dragend", onDragEnd);

#### Attach dragEnd event handler via bind(); detach via unbind()

    // event handler for dragEnd
    var onDragEnd = function(e) {
        // ...
    };
    
    // attach dragEnd event handler via bind()
    $("#window").data("kendoWindow").bind("dragend", onDragEnd);
    
    // detach dragEnd event handler via unbind()
    $("#window").data("kendoWindow").unbind("dragend", onDragEnd);

### dragstart

Triggered when the user starts to move the window.

### error

Triggered when an AJAX request for content fails.

#### Attach error event handler during initialization; detach via unbind()

    // event handler for error
    var onError = function(e) {
        // ...
    };
    
    // attach dragEnd event handler during initialization
    var kendoWindow = $("#window").kendoWindow({
        error: onError
    });
    
    // detach error event handler via unbind()
    kendoWindow.data("kendoWindow").unbind("error", onError);

#### Attach error event handler via bind(); detach via unbind()

    // event handler for error
    var onError = function(e) {
        // ...
    };
    
    // attach error event handler via bind()
    $("#window").data("kendoWindow").bind("error", onError);
    
    // detach error event handler via unbind()
    $("#window").data("kendoWindow").unbind("error", onError);

### open

Triggered when a Window is opened (i.e. the open() method is called).

#### Attach open event handler during initialization; detach via unbind()

    // event handler for expand
    var onOpen = function(e) {
        // ...
    };
    
    // attach open event handler during initialization
    var kendoWindow = $("#window").kendoWindow({
        open: onOpen
    });
    
    // detach expand event handler via unbind()
    kendoWindow.data("kendoWindow").unbind("open", onOpen);

#### Attach open event handler via bind(); detach via unbind()

    // event handler for open
    var onOpen = function(e) {
        // ...
    };
    
    // attach open event handler via bind()
    $("#window").data("kendoWindow").bind("open", onOpen);
    
    // detach open event handler via unbind()
    $("#window").data("kendoWindow").unbind("open", onOpen);

### refresh

Triggered when the content of a Window have been refreshed via AJAX.

#### Attach refresh event handler during initialization; detach via unbind()

    // event handler for refresh
    var onRefresh = function(e) {
        // ...
    };
    
    // attach refresh event handler during initialization
    var kendoWindow = $("#window").kendoWindow({
        refresh: onRefresh
    });
    
    // detach refresh event handler via unbind()
    kendoWindow.data("kendoWindow").unbind("refresh", onRefresh);

#### Attach refresh event handler via bind(); detach via unbind()

    // event handler for refresh
    var onRefresh = function(e) {
        // ...
    };
    
    // attach refresh event handler via bind()
    $("#window").data("kendoWindow").bind("refresh", onRefresh);
    
    // detach refresh event handler via unbind()
    $("#window").data("kendoWindow").unbind("refresh", onRefresh);

### resize

Triggered when a Window has been resized by a user.

#### Attach resize event handler during initialization; detach via unbind()

    // event handler for resize
    var onResize = function(e) {
        // ...
    };
    
    // attach resize event handler during initialization
    var kendoWindow = $("#window").kendoWindow({
        resize: onResize
    });
    
    // detach resize event handler via unbind()
    kendoWindow.data("kendoWindow").unbind("resize", onResize);

#### Attach resize event handler via bind(); detach via unbind()

    // event handler for resize
    var onResize = function(e) {
        // ...
    };
    
    // attach resize event handler via bind()
    $("#window").data("kendoWindow").bind("resize", onResize);
    
    // detach resize event handler via unbind()
    $("#window").data("kendoWindow").unbind("resize", onResize);
