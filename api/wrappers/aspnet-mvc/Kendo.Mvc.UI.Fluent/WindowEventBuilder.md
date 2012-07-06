---
title:Kendo.Mvc.UI.Fluent.WindowEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.windoweventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.WindowEventBuilder

## Methods

### Error(System.Func{System.Object,System.Object})
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events => events.Error("onError"))
        %>

#### Parameters

##### handlerName `System.Func{System.Object`
The name of the JavaScript function that will handle the event.