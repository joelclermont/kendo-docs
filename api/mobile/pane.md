---
title: kendo.mobile.ui.Pane
slug: mobile-kendo.mobile.ui.pane
tags: api,mobile
publish: true
---

# kendo.mobile.ui.Pane

## Configuration

### initial `String`

 The id of the initial mobilie View to display.

### layout `String`

 The id of the default Pane Layout.

### loading `String`*(default: Loading...)*

 The text displayed in the loading popup. Setting this value to false will disable the loading popup.

### transition `String`

 The default View transition.

## Methods

### hideLoading

Hide the loading animation.

### navigate

Navigate the local or remote view.

#### Navigate to a remote view

    <div data-role="pane" id="main-pane">
    </div>
    
    <script>
    var pane = $("#main-pane").data("kendoMobilePane");
    pane.navigate("settings.html");
    </script>

#### Navigate to a local view

    <div data-role="pane" id="main-pane">
      <div data-role="view" id="foo"> ... </div>
    </div>
    
    <script>
    var pane = $("#main-pane").data("kendoMobilePane");
    pane.navigate("#foo");
    </script>

#### Parameters

##### url `String`

The id or url of the view.

##### transition `String`

The transition to apply when navigating. See View Transitions section for more
information.

### showLoading

Show the loading animation.

### view

Get a reference to the current view.

#### Returns

`View` the view instance.

## Events

### navigate

Fires when pane navigates to a view.

#### Event Data

##### e.url `jQuery`

The url of the view

### viewShow

Fires after the pane displays a view.

#### Event Data

##### e.view `View`

The displayed view
