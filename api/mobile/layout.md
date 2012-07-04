---
title: kendo.mobile.ui.Layout
slug: mobile-kendo.mobile.ui.layout
tags: api,mobile
publish: true
---

# kendo.mobile.ui.Layout

## Description



A mobile **Layout** is used to share headers and footers between multiple **Views**.
The header and/or footer element of the **Layout** are applied to any **View** that uses it.

To define a **Layout** set `data-role="layout"` to an element.

<p>When a view with the given layout is displayed, the layout attaches its header and footer to it.

**Note:** When instantiated, the layout detaches its element from the document tree.

A **View** is associated with a **Layout** by setting its `data-layout` attribute value
to the value of the layout's `data-id` attribute:

#### Views with Layout

    <div data-role="view" data-layout="foo">Foo</div>
    <div data-role="view" data-layout="foo">Bar</div>
    
    <div data-role="layout" data-id="foo">
      <div data-role="header">Header</div>
      <div data-role="footer">Footer</div>
    </div>

A default **Application** layout can be set by passing the layout id in the `options` parameter of the **Application**'s constructor.
A mobile **View** can remove the default application **Layout** by setting `data-layout=""`.

#### Default Application Layout

    <div data-role="view">Bar</div>
    
    <div data-role="layout" data-id="foo">
      <div data-role="header">Header</div>
    </div>
    
    <script>
       new kendo.mobile.Application($(document.body), { layout: "foo" });
    </script>

Layouts can be platform specific, allowing for different layout and behavior per platform.
A layout platform can be specified using `data-platform=""`

#### iOS and Android Application Layout

    <div data-role="view">Bar</div>
    
    <div data-role="layout" data-id="foo" data-platform="ios">
      <div data-role="header">Header</div>
    </div>
    
    <div data-role="layout" data-id="foo" data-platform="android">
      <div data-role="header">Header</div>
    </div>

### Layout DOM elements

Each mobile Layout instance exposes the following fields:

*   **header** - the header DOM element;
*   **footer** - the footer DOM element;

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