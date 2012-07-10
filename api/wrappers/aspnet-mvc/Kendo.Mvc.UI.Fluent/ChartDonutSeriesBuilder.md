---
title:ChartDonutSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdonutseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDonutSeriesBuilder

Defines the fluent interface for configuring donut series.

## Methods

### Margin(System.Int32)
Sets the margin of the donut series.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Donut(s => s.Sales, s => s.DateString).Margin(10))
        .Render();
        %>

### HoleSize(System.Int32)
Sets the the size of the donut hole.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Donut(s => s.Sales, s => s.DateString).HoleSize(40))
        .Render();
        %>

### Size(System.Int32)
Sets the size of the donut series.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Donut(s => s.Sales, s => s.DateString).Size(20))
        .Render();
        %>