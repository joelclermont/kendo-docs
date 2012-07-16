---
title: kendo.mobile.ui.View
slug: mobile-kendo.mobile.ui.view
tags: api,mobile
publish: true
---

# kendo.mobile.ui.View

## Configuration

### model `String | ObservableObject`*(default: null)*

 The MVVM model to bind to. If a string is passed, The view
will try to resolve a reference to the view model variable in the global scope.

#### Example

    <script>
     var foo = { bar: "baz" }
    </script>

    <div data-role="view" data-model="foo">
       <span data-bind="text:bar"></span>
    </div>

### stretch `Boolean`*(default: false)*

 If set to true, the view will stretch its child contents to occupy the entire view, while disabling kinetic scrolling.
Useful if the view contains an image or a map.

### title `String`

 The text to display in the navbar title (if present) and the browser title.

## Events

### beforeShow

Fires before the mobile View becomes visible. The event can be prevented by calling the `preventDefault` method of the event parameter, in case a redirection should happen.

#### Event Data

##### e.view `jQuery`

The mobile view instance

### hide

Fires when the mobile View becomes hidden.

#### Event Data

##### e.view `jQuery`

The mobile view instance

### init

Fires after the mobile View and its child widgets are initialized.

#### Event Data

##### e.view `jQuery`

The mobile view instance

### show

Fires when the mobile View becomes visible.

#### Event Data

##### e.view `jQuery`

The mobile view instance
