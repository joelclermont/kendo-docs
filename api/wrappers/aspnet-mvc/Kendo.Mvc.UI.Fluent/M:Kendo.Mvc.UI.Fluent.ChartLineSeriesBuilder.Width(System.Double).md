---
title:Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder

## Methods

### Width(System.Double)
Sets the line chart line width.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Line(s => s.Sales).Width(2))
        .Render();
        %>

#### Parameters

##### width `System.Double`
The line width.