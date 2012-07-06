---
title:Kendo.Mvc.UI.Fluent.ChartEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charteventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartEventBuilder

## Methods

### AxisLabelClick(System.String)
Defines the name of the JavaScript function that will handle the the AxisLabelClick client-side event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.AxisLabelClick("onAxisLabelClick"))
        %>

#### Parameters

##### onAxisLabelClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.