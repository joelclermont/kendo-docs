---
title:Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder

## Methods

### Padding(System.Int32)
Sets the padding of the chart.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).Padding(100))
        .Render();
        %>