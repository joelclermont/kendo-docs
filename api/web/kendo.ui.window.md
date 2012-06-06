## Description


kendo.ui.Window.Description

 A **Window** displays content in a modal or non-modal HTML window. By default, a
 **Window** can be moved, resized, and closed. Its content can also be defined with either as
 static HTML or loaded dynamically via AJAX.



 A **Window** can be initialized from virtually any DOM element. During initialization, the
 targeted content will automatically be wrapped in the div element of the **Window**.


### Getting Started

#### Create a simple HTML element with the Window content

    <div id="window">
        Content of the Window
    </div>


#### Initialize the Window using a selector

    $(document).ready(function() {
        $("#window").kendoWindow();
    });


 When a **Window** is initialized, it will automatically be displayed open near the location of the
 DOM element that was used to initialize the content.


### Configuring Window Behaviors


 A **Window** provides many configuration options that can be easily set during initialization.
 Among the properties that can be controlled:


*   Minimum height/width
*   Available user actions (close/refresh/maximize/minimize) and ability to define custom ones
*   Title
*   Draggable and resizable behaviors

#### Create a modal Window with all user actions enabled

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

#### Custom actions

      $("#window").kendoWindow({
          actions: ["Custom", "Minimize", "Maximize", "Close"],
          title: "Window Title"
      }).data("kendoWindow").wrapper.find(".k-custom").click(function(e) {
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


#### Centering a Window and opening on button click

    <div id="window">
        Content of the Window
    </div>
    <button id="openButton">Open Window</button>


#### Initialize Window, center, and configure button click action

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


### Loading Window content via AJAX


 A **Window** provides built-in support for asynchronously loading content from a URL. This URL
 should return a HTML fragment that can be loaded in a Window content area.

#### Load Window content asynchronously

    <div id="window"></div>


#### Initialize window and configure content loading

    $(document).ready(function(){
        $("#window").kendoWindow({
            content: "html-content-snippet.html",
            title: "Async Window Content"
        });
    });


### Accessing an Existing Window


 You can reference an existing **Window** instance via
 [jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
 use the API to control its behavior.

#### Accessing an existing Window instance

    var win = $("#window").data("kendoWindow");



------------------------------------------

## Configuration

### `actions` : **Array** *(default: ["Close"])* 

The buttons for interacting with the window. Predefined array values are "Close", "Refresh", "Minimize",and "Maximize".

### `animation` : **Object**  

A collection of {Animation} objects, used to change default animations. A value of <strong>false</strong>will disable all animations in the widget.

### `animation.close` : **Animation**  

The animation that will be used when a Window closes.

### `animation.open` : **Animation**  

The animation that will be used when a Window opens.

### `appendTo` : **Object** *(default: document.body)* 

The element that the Window will be appended to.

### `content` : **Object|String**  

Specifies a URL or request options that the window should load its content from. For remote URLs, acontainer iframe element is automatically created.

### `content.template` : **String**  

Template for the content of a <strong>Window</strong>.

### `draggable` : **Boolean** *(default: true)* 

Enables (<strong>true</strong>) or disables (<strong>false</strong>) the ability for users to move/drag a<strong>Window</strong>.

### `iframe` : **Boolean**  

Explicitly states whether content iframe should be created.

### `maxHeight` : **Integer** *(default: Infinity)* 

The maximum height (in pixels) that may be achieved by resizing the window.

### `maxWidth` : **Integer** *(default: Infinity)* 

The maximum width (in pixels) that may be achieved by resizing the window.

### `minHeight` : **Integer** *(default: 50)* 

The minimum height (in pixels) that may be achieved by resizing the window.

### `minWidth` : **Integer** *(default: 50)* 

The minimum width (in pixels) that may be achieved by resizing the window.

### `modal` : **Boolean** *(default: false)* 

Specifies whether the window should show a modal overlay over the page.

### `resizable` : **Boolean** *(default: true)* 

Enables (<strong>true</strong>) or disables (<strong>false</strong>) the ability for users to resize a<strong>Window</strong>.

### `title` : **String**  

The text in the window title bar.

### `visible` : **Boolean** *(default: true)* 

Specifies whether the window will be initially visible.



------------------------------------------

## Methods

### `center`()`Window`


Centers a **Window** within the viewport.

#### Example

    var kendoWindow = $("#window").data("kendoWindow");
    kendoWindow.center();

#### Returns 

`Window` Returns the (Kendo UI) Window object to support chaining.

### `close`()`Window`


Closes a Window.

#### Close a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").close();

#### Returns 

`Window` Returns the (Kendo UI) Window object to support chaining.

### `content`(content)`Window`


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

### `destroy`()


Destroys the window and its modal overlay, if necessary. Useful for removing modal windows.
### `maximize`()`Window`


Maximizes a Window to the entire viewing area of the user agent.



#### Maximize a Window

    $("#window").data("kendoWindow").maximize();

#### Returns 

`Window` Returns the (Kendo UI) Window object to support chaining.

### `minimize`()`Window`


Maximizes a Window to its title bar.



#### Minimize a Window

    $("#window").data("kendoWindow").minimize();

#### Returns 

`Window` Returns the (Kendo UI) Window object to support chaining.

### `open`()`Window`


Opens a Window.

#### Open a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").open();

#### Returns 

`Window` Returns the (Kendo UI) Window object to support chaining.

### `refresh`(options)`Window`


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

### `restore`()`Window`


Restores a maximized or minimized Window to its previous state.

#### Restore the state of a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").restore();

#### Returns 

`Window` Returns the (Kendo UI) Window object to support chaining.

### `title`(text)`Window`


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

### `toFront`()`Window`


Brings forward a Window to the top of the z-index.

#### Bring forward a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").toFront();

#### Returns 

`Window` Returns the (Kendo UI) Window object to support chaining.

### `toggleMaximization`()`Window`


Toggles a Window between a maximized and restored state.

#### Toggle the state of a Window; utilize chaining (if necessary)

    var kendoWindow = $("#window").data("kendoWindow").toggleMaximization();

#### Returns 

`Window` Returns the (Kendo UI) Window object to support chaining.



------------------------------------------

## Events

### `activate`
Triggered when a Window has finished its opening animation.

kendo.ui.Window#activate



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

### `close`
Triggered when a Window is closed (by a user or through the close() method).

kendo.ui.Window#close





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

### `deactivate`
Triggered when a Window has finished its closing animation.

kendo.ui.Window#deactivate



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

### `dragend`
Triggered when a Window has been moved by a user.

kendo.ui.Window#dragend



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

### `dragstart`
Triggered when the user starts to move the window.

kendo.ui.Window#dragstart


### `error`
Triggered when an AJAX request for content fails.

kendo.ui.Window#error



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

### `open`
Triggered when a Window is opened (i.e. the open() method is called).

kendo.ui.Window#open





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

### `refresh`
Triggered when the content of a Window have been refreshed via AJAX.

kendo.ui.Window#refresh



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

### `resize`
Triggered when a Window has been resized by a user.

kendo.ui.Window#resize



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

