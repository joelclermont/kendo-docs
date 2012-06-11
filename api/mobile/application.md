# kendo.mobile.Application

## Description



The Kendo mobile **Application** provides the necessary tools for building native-looking web based mobile applications.

### Getting Started

The simplest mobile **Application** consists of a single mobile **View**. 

#### Hello World mobile Application

    <body>
       <div data-role="view">
         <div data-role="header">Header</div>
         Hello world!
         <div data-role="footer">Footer</div>
       </div>
    
       <script>
       var app = new kendo.mobile.Application(); //document.body is used by default
       </script>
    </body>

### Mobile Views


<p>The mobile **Application** consists of a single HTML page with one or more mobile Views, linked with navigational widgets (Buttons, TabStrip, etc.).
Each child of the application element (`&lt;body&gt;` by default) with `data-role="view"` is considered a mobile view.

### Navigation

When initialized, the mobile **Application** modifies the kendo mobile widgets' (listview link items, buttons, tabs, etc.) behavior so that they navigate between the mobile views when the user taps them.
When targeting local views, The navigation **Widget**'s `href` attribute specifies the **View** id to navigate to, prefixed with `#`, like an anchor.

#### Views linked with mobile Buttons

    <div data-role="view" id="foo">Foo <a href="#bar" data-role="button">Go to Bar</a></div>
    <div data-role="view" id="bar">Bar <a href="#foo" data-role="button">Go to Foo</a></div>

### Linking to External Pages

By default, all navigational widgets try to navigate to loacal views when tapped. This behavior can be overridden by setting `data-rel="external"` attribute to the link element. 

#### External links

    <a href="http://kendoui.com/" data-rel="external">Visit KendoUI</a>

### View Transitions

**View** transitions are defined by setting a `data-transition` attribute to the **View** DOM element or to the navigational widget `A` DOM element.
If both are present, the navigational widget transition takes precedence.
An application-wide default transition may be set using the `transition` parameter in the options parameter of the **Application** constructor.
The following transitions are supported:

#### slide

 This is the default iOS **View** transition. Old **View** content slides to the left and the new **View** content slides in its place.
Headers and footers (if present) use the **fade** transition. 

The transition direction can be specified by using `slide:(direction)`.
Supported directions are `left` and `right`. By default, the direction is `left`.

#### zoom

The new **View** (along with its header and footer) content zooms from the center of the previous **View**. The old **View** content fades out. Suitable for displaying dialogs.

#### fade

The new **View** (along with its header and footer) content fades in on top of the previous **View** content.

#### overlay

The new **View** content slides on top of the previous **View**. Unlike the `slide` transition,
the previous View stays "under" the new one, and the headers / footers do not transition separately. 

The transition direction can be specified by using `overlay:(direction)` format.
Supported directions are `down`, `left`, `up` and `right`. By default, the direction is `left`.

#### Views with Transitions

    <div data-role="view" id="foo" data-transition="slide">Foo <a href="#bar" data-role="button">Go to Bar</a></div>
    <div data-role="view" id="bar" data-transition="overlay:up">Bar <a href="#foo" data-role="button">Go to Foo</a></div>

Each transition may be played in **reverse**. To do so, add `" reverse"` after the transition definition. For
instance, to simulate returning to previous view using slide transition, use `"slide:left reverse"`

#### Reverse transition

    <div data-role="view" id="foo">Foo <a href="#bar" data-role="button">Go to Bar</a></div>
    <div data-role="view" id="bar">Bar <a href="#foo" data-role="button" data-transition="slide:left reverse">Go to Foo</a></div>

When a **View** transitions to the **View** displayed before it (foo → bar → foo), this is considered a **back** navigation.
In this case, the animation of the current **View** is applied in reverse.
For instance, navigating with slide transition from `foo` to `bar`, then back to `foo`
would cause the `foo` **View** to slide from the right side of the screen. 

### Remote Views

The Kendo mobile **Application** can load **Views** remotely, using AJAX. If the navigational widget href attribute value does not start with a hash (#),
the application considers the View to be remote, and issues an AJAX request to the provided URL.

The View content (the first element with `data-role="view"`) is extracted from the AJAX response and appended into the Application DOM element.
Once the remote **View** is fetched, no additional round trips to the server occur when the **View** is displayed again. 

#### Remote View

    <!-- foo.html -->
    <div data-role="view">Foo <a href="bar.html" data-role="button">Go to Bar</a></div>
    
    <!-- bar.html -->
    <div data-role="view">Bar</div>

The remote view request will also append (but not initialize) any **additional views** found in the AJAX
response. **Inline style** elements, **inline script** elements, and **mobile layout** definitions will also be evaluated and appended to the
application. The elements must be available in the root of the response, or nested inside the **body** element. 

Scripts and styles from the **head** element (if present) will **not** be evaluated.

If the remote view needs an **additional scripting (widget initialization/binding)** logic, it may be defined in the view init event handler,  in the AJAX response.

#### Remote view with init event handler

    <!-- foo.html -->
    <div data-role="view">
    <a data-role="button" href="bar.html">Go to bar</a>
    </div>
    
    <!-- bar.html -->
    <div data-role="view" data-init="initBar">
      <a href="#" id="link">Link</a>
    </div>
    
    <script>
      function initBar(e) {
          e.view.element.find("#link").kendoMobileButton();
      }
    </script>

###  Initial View


<p> The **Application** provides a way to specify the initial view to show. The initial view can be set by
passing the view id in the options parameter of the Application's constructor:

#### Define initial view

    <script>
         new kendo.mobile.Application($(document.body), {
             initial: "ViewID"
         });
    </script>

### Web Clip Icons

The mobile devices can create a bookmark with a custom icon, placed on the Home screen. Users can use the shortcut to open that web page later.

#### Define web clip icon

    <script>
         new kendo.mobile.Application($(document.body), {
             icon: "URL to a web clip icon"
         });
    </script>

Multiple icons for different sizes can be defined. Please refer to Apple [Web Clip Icons help topic](https://developer.apple.com/library/ios/#documentation/userexperience/conceptual/mobilehig/IconsImages/IconsImages.html#//apple_ref/doc/uid/TP40006556-CH14-SW11)
for more information.

#### Define multiple web clip icons

    <script>
         new kendo.mobile.Application($(document.body), {
             icon: {
               "72x72" : "URL to a 72 x 72 pixels web clip icon",
               "114x114" : "URL to a 114 x 114 pixels web clip icon"
             }
         });
    </script>

### Force Platform Styles


<p> The **Application** provides a way to force a specific platform look on your application upon init by
passing the OS name in the options parameter of the Application's constructor:

#### Force iOS look

    <script>
         new kendo.mobile.Application($(document.body), {
             platform: "ios"
         });
    </script>

Additionally, the OS version can be specified by by passing kendo.support.mobileOS object that is expected by Kendo UI Mobile.
This is more complex, but allows fine grained tuning of the application look and behavior. A sample object initialization is like this:

#### Force iOS 5 look

    <script>
         new kendo.mobile.Application($(document.body), {
             platform: {
                            device: "ipad",       // Mobile device, can be "ipad", "iphone", "ipod", "android" "fire", "blackberry", "meego"
                            name: "ios",          // Mobile OS, can be "ios", "android", "blackberry", "meego"
                            ios: true,            // Mobile OS name as a flag
                            majorVersion: 5,      // Major OS version
                            minorVersion: "0.0",  // Minor OS versions
                            flatVersion: "500",   // Flat OS version for easier comparison
                            appMode: false        // Whether running in browser or in AppMode/PhoneGap/Titanium.
                            tablet: "ipad"        // If a tablet - tablet name or false for a phone.
                       }
         });
    </script>

## Configuration

### `hideAddressBar` : **Boolean** *(default: true)*

 Whether to hide the browser address bar.
<script>
     new kendo.mobile.Application($(document.body), { layout: "foo" });
</script>

### `initial` : **String** 

 The id of the initial mobilie View to display.

#### Example

    <script>
         new kendo.mobile.Application($(document.body), {
             initial: "ViewID"
         });
    </script>

### `layout` : **String** 

 The id of the default Application Layout.

#### Example

    <div data-role="view">Bar</div>
    
    <div data-role="layout" data-id="foo">
      <div data-role="header">Header</div>
    </div>

### `loading` : **String** *(default: Loading...)*

 The text displayed in the loading popup. Setting this value to false will disable the loading popup.

### `platform` : **String** 

 Which platform look to force on the application. Can be one of "ios", "android", "blackberry".

#### Example

    <script>
         new kendo.mobile.Application($(document.body), {
             platform: "android"
         });
    </script>

### `transition` : **String** 

 The default View transition.

#### Example

    <script>
         new kendo.mobile.Application($(document.body), { transition: "slide" });
    </script>

## Methods

### hideLoading

Hide the loading animation.

#### Example

    <script>
      var app = new kendo.mobile.Application();
      app.hideLoading();
    </script>

### navigate

Navigate to local or to remote view.

#### Navigate to a remote view

    var app = new kendo.mobile.Application();
    app.navigate("settings.html");

#### Navigate to a local view

    <div data-role="view" id="foo"> ... </div>
    
    <script>
    var app = new kendo.mobile.Application();
    app.navigate("#foo");
    </script>

#### Parameters

##### url `String`

The id or url of the view.

##### transition `String`

The transition to apply when navigating. See View Transitions section for more
information.

### scroller

Get a reference to the current view's scroller widget instance.

#### Returns

`Scroller` the scroller widget instance.

### showLoading

Show the loading animation.

#### Example

    <script>
      var app = new kendo.mobile.Application();
      app.showLoading();
    </script>

### view

Get a reference to the current view.

#### Returns

`View` the view instance.

## Events