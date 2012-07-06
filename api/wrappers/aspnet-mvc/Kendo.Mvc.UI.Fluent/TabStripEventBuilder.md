---
title:Kendo.Mvc.UI.Fluent.TabStripEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.tabstripeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TabStripEventBuilder

## Methods

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.Error("onError"))
        %>

#### Parameters

##### onErrorHandlerName `System.String`
The name of the JavaScript function that will handle the event.