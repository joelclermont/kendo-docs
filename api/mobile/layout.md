---
title: kendo.mobile.ui.Layout
slug: mobile-kendo.mobile.ui.layout
tags: api,mobile
publish: true
---

# kendo.mobile.ui.Layout

## Configuration

### id `String`*(default: null)*

 The id of the layout. Required.

### platform `String`

 The specific platform this layout targets. By default, layouts are displayed
on all platforms.

## Events

### hide

Fires when a mobile View using the layout becomes hidden.

#### Event Data

##### e.layout `jQuery`

The mobile layout instance

##### e.view `jQuery`

The mobile view instance

### init

Fires after a mobile Layout and its child widgets is initialized.

#### Event Data

##### e.layout `jQuery`

The mobile layout instance

### show

Fires when a mobile View using the layout becomes visible.

#### Event Data

##### e.layout `jQuery`

The mobile layout instance

##### e.view `jQuery`

The mobile view instance
