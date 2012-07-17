---
title: kendo.mobile.ui.PopOver
slug: mobile-kendo.mobile.ui.popover
tags: api,mobile
publish: true
---

# kendo.mobile.ui.PopOver

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
