---
title:Kendo.Mvc.UI.Fluent.ChartEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charteventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartEventBuilder

## Methods

### DataBound(System.String)
Defines the name of the JavaScript function that will handle the the DataBound client-side event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.DataBound("onDataBound"))
        %>

#### Parameters

##### onDataBoundHandlerName `System.String`
The name of the JavaScript function that will handle the event.