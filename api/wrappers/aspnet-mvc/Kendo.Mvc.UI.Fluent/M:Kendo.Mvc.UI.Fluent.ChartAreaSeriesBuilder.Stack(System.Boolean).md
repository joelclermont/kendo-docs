---
title:Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareaseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder

## Methods

### Stack(System.Boolean)
Sets a value indicating if the areas should be stacked.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Area(s => s.Sales).Stack(true))
        %>

#### Parameters

##### stacked `System.Boolean`
A value indicating if the areas should be stacked.