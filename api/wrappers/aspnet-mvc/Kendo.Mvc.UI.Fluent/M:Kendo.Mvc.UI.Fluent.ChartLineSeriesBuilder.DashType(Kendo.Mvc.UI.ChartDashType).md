---
title:Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder

## Methods

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the line chart line dash type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Line(s => s.Sales).DashType(ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dash type.