---
title:Kendo.Mvc.UI.Fluent.PanelBarEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.panelbareventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PanelBarEventBuilder

## Methods

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Error("onError"))
        %>

#### Parameters

##### errorHandlerName `System.String`
The name of the JavaScript function that will handle the event.