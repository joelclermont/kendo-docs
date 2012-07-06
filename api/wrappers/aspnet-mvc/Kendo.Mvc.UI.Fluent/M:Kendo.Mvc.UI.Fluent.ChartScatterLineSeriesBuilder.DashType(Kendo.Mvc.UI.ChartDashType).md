---
title:Kendo.Mvc.UI.Fluent.ChartScatterLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterLineSeriesBuilder

## Methods

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the chart line dash type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.ScatterLine(s => s.x, s => s.y).DashType(ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dash type.