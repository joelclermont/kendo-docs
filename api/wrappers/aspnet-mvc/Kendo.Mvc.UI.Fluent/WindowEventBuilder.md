---
title:WindowEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.windoweventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.WindowEventBuilder

Defines the fluent interface for configuring the Window events.

## Methods

### Open(System.String)
Defines the name of the JavaScript function that will handle the the Open client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Open("onOpen"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### Open(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Open client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Open("onOpen"))
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The name of the JavaScript function that will handle the event.

### Activate(System.String)
Defines the name of the JavaScript function that will handle the the Activate client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Activate("onActivate"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### Activate(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Activate client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Activate("onActivate"))
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The name of the JavaScript function that will handle the event.

### Deactivate(System.String)
Defines the name of the JavaScript function that will handle the the Deactivate client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Deactivate("onDeactivate"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### Deactivate(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Deactivate client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Deactivate("onDeactivate"))
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The name of the JavaScript function that will handle the event.

### Close(System.String)
Defines the name of the JavaScript function that will handle the the Close client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Close("onClose"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### Close(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Close client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Close("onClose"))
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The name of the JavaScript function that will handle the event.

### DragStart(System.String)
Defines the name of the JavaScript function that will handle the the DragStart client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.DragStart("onDragStart"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### DragStart(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the DragStart client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.DragStart("onDragStart"))
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The name of the JavaScript function that will handle the event.

### DragEnd(System.String)
Defines the name of the JavaScript function that will handle the the DragEnd client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.DragEnd("onDragEnd"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### DragEnd(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the DragEnd client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.DragEnd("onDragEnd"))
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The name of the JavaScript function that will handle the event.

### Resize(System.String)
Defines the name of the JavaScript function that will handle the the Resize client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Resize("onResize"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### Resize(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Resize client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Resize("onResize"))
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The name of the JavaScript function that will handle the event.

### Refresh(System.String)
Defines the name of the JavaScript function that will handle the the Refresh client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Refresh("onRefresh"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### Refresh(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Refresh client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Refresh("onRefresh"))
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The name of the JavaScript function that will handle the event.

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Error("onError"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### Error(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Error("onError"))
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The name of the JavaScript function that will handle the event.