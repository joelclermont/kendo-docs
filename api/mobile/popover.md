---
title: kendo.mobile.ui.PopOver
tags: api,mobile
publish: true
---

# kendo.mobile.ui.PopOver

## Description



The mobile PopOver widget represents a transient view which is displayed when the user taps on a navigational widget
or area on the screen. It can contain one or more mobile views which can be navigated to, if needed.
The Mobile Application automatically instantiates a mobile PopOver for each div element with a `role`
data attribute set to **popover**.
Alternatively, it can be initialized using jQuery plugin syntax in the containing mobile View **init event handler**.


The Mobile PopOver widget can be open when any mobile navigational widget (listview link item, button, tabstrip, etc.) is tapped.
To do so, add `data-rel="popover"` attribute and a `href` attribute equal to the PopOver `id` to the navigational widget DOM element (prefixed with `#`, like an anchor).

#### A Mobile PopOver displaying "Hello World"

    <div data-role="view">
     <a data-role="button" href="#foo" data-rel="popover">Say Hello</a>
    
     <div data-role="popover">
         <div data-role="view">
             Hello world!
         </div>
     </div>
    </div>

The Mobile PopOver widget implicitly instantiates a pane widget for its contents, which allows the containing views to navigate to each
other. The pane widget behavior (including default transition, layout, etc.) may be configured from the `pane` configuration option.

The popover dimensions and direction can be configured from the `popup` configuration option.

## Configuration

### pane `Object`

The pane configuration options.

### pane.initial `String`

 The id of the initial mobile View to display.

### pane.layout `String`

 The id of the default Pane Layout.

### pane.loading `String`*(default: Loading...)*

 The text displayed in the loading popup. Setting this value to false will disable the loading popup.

### pane.transition `String`

 The default View transition.

### popup `Object`

The popup configuration options.

### popup.direction `Number | String`*(default: down)*

 The direction to which the popup will expand, relative to the target that opened it.
Supported directions are up, right, down, and left.

### popup.height `Number | String`*(default: 320)*

 The height of the popup in pixels.

### popup.width `Number | String`*(default: 240)*

 The width of the popup in pixels.

## Methods

### close

Close the popover.

#### Close a popover when a button is clicked

    <div data-role="popover" id="foo">
     <a data-role="button" data-click="closePopOver">Close</a>
    </div>
    
    <script>
     function closePopOver() {
         $("#foo").data("kendoMobilePopOver").close();
     }
    </script>

### openFor

Open the ActionSheet.

#### Parameters

##### target `jQuery`

The target of the Popover, to which the visual arrow will point to.

## Events

### close

Fires when popover is closed.

### open

Fires when popover is opened.