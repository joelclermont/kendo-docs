---
title:Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder

## Methods

### StartAngle(System.Int32)
Sets the start angle of the first pie segment.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).StartAngle(100))
        .Render();
        %>

#### Parameters

##### startAngle `System.Int32`
The pie start angle(in degrees).