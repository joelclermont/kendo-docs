---
title:Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder

## Methods

### Name(System.String)
Sets the name of the series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).Name("Sales"))
        %>