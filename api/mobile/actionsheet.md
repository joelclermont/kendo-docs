---
title: kendo.mobile.ui.ActionSheet
slug: mobile-kendo.mobile.ui.actionsheet
tags: api,mobile
publish: true
---

# kendo.mobile.ui.ActionSheet

## Configuration

### cancel `String`*(default: Cancel)*

 The text of the cancel button.

### popup `Object`

The popup configuration options (tablet only).

### popup.direction `Number | String`*(default: down)*

 The direction to which the popup will expand, relative to the target that opened it.

### popup.height `Number | String`*(default: auto)*

 The height of the popup in pixels.

### popup.width `Number | String`*(default: 240)*

 The width of the popup in pixels.

## Methods

### close

Close the ActionSheet.

### open

Open the ActionSheet.

#### Parameters

##### target `jQuery`

(optional) The target of the ActionSheet, available in the callback methods.

##### context `Object`

(optional) The context of the ActionSheet, available in the callback methods.

## Events

### open

Fires when the ActionSheet is opened.

#### Event Data

##### e.target `jQuery`

The invocation target of the ActionSheet.

##### e.context `jQuery`

The defined ActionSheet context.
