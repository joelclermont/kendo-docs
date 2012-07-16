---
title: kendo.mobile.Application
slug: mobile-kendo.mobile.application
tags: api,mobile
publish: true
---

# kendo.mobile.Application

## Configuration

### hideAddressBar `Boolean`*(default: true)*

Whether to hide the browser address bar.

#### Example
    <script>
         new kendo.mobile.Application($(document.body), { hideAddressBar: false });
    </script>

### initial `String`

 The id of the initial mobilie View to display.

#### Example

    <script>
         new kendo.mobile.Application($(document.body), {
             initial: "ViewID"
         });
    </script>

### layout `String`

 The id of the default Application Layout.

#### Example

    <div data-role="view">Bar</div>

    <div data-role="layout" data-id="foo">
      <div data-role="header">Header</div>
    </div>

### loading `String`*(default: Loading...)*

 The text displayed in the loading popup. Setting this value to false will disable the loading popup.

### platform `String`

 Which platform look to force on the application. Can be one of "ios", "android", "blackberry".

#### Example

    <script>
         new kendo.mobile.Application($(document.body), {
             platform: "android"
         });
    </script>

### transition `String`

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
