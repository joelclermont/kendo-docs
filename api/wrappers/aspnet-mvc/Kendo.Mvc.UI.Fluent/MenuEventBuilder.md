---
title:Kendo.Mvc.UI.Fluent.MenuEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.menueventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.MenuEventBuilder

## Methods

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Select("onSelect"))
        %>

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.