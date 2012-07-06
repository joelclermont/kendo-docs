---
title:Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase

## Methods

### XAxis(System.String)
Sets the axis name to use for this series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Scatter(s => s.X, s => s.Y).Name("Scatter").XAxis("secondary"))
        .XAxis(axis => axis.Numeric())
        .XAxis(axis => axis.Numeric("secondary"))
        %>

#### Parameters

##### axis `System.String`
The axis name for this series.