---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### SeriesDefaults(System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesDefaultsBuilder{`0}})
Defines the options for all chart series of the specified type.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .SeriesDefaults(series => series.Bar().Stack(true))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesDefaultsBuilder{`0}}`
The configurator.