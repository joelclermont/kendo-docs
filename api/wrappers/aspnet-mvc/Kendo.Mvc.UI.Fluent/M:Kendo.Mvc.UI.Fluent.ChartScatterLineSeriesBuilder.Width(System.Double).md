---
title:Kendo.Mvc.UI.Fluent.ChartScatterLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterLineSeriesBuilder

## Methods

### Width(System.Double)
Sets the chart line width.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.ScatterLine(s => s.x, s => s.y).Width(2))
        .Render();
        %>

#### Parameters

##### width `System.Double`
The line width.