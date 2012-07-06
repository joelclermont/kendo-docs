---
title:Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase

## Methods

### YAxis(System.String)
Sets the axis name to use for this series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Scatter(s => s.Sales).Name("Sales").YAxis("secondary"))
        .YAxis(axis => axis.Numeric())
        .YAxis(axis => axis.Numeric("secondary"))
        %>

#### Parameters

##### axis `System.String`
The axis name for this series.