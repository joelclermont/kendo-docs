---
title:Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase

## Methods

### Axis(System.String)
Sets the axis name to use for this series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Name("Sales").Axis("secondary"))
        .ValueAxis(axis => axis.Numeric())
        .ValueAxis(axis => axis.Numeric("secondary"))
        .CategoryAxis(axis => axis.AxisCrossingValue(0, 10))
        %>

#### Parameters

##### axis `System.String`
The axis name for this series.