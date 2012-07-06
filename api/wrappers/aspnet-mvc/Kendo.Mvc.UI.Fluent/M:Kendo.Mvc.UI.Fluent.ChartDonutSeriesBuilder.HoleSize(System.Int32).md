---
title:Kendo.Mvc.UI.Fluent.ChartDonutSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdonutseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDonutSeriesBuilder

## Methods

### HoleSize(System.Int32)
Sets the the size of the donut hole.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Donut(s => s.Sales, s => s.DateString).HoleSize(40))
        .Render();
        %>