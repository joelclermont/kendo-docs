---
title:Kendo.Mvc.UI.Fluent.ChartDonutSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdonutseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDonutSeriesBuilder

## Methods

### Margin(System.Int32)
Sets the margin of the donut series.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Donut(s => s.Sales, s => s.DateString).Margin(10))
        .Render();
        %>