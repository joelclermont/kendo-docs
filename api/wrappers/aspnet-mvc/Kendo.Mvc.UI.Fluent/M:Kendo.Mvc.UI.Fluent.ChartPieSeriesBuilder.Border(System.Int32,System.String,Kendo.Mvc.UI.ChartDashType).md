---
title:Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the pie segments border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The pie segments border width.

##### color `System.String`
The pie segments border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The pie segments border dash type.