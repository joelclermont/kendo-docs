---
title:Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder

## Methods

### Stack(System.Boolean)
Sets a value indicating if the lines should be stacked.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Line(s => s.Sales).Stack(true))
        %>

#### Parameters

##### stacked `System.Boolean`
A value indicating if the lines should be stacked.