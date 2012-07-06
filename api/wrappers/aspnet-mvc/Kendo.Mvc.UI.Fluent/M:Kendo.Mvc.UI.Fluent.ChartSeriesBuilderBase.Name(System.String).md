---
title:Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase

## Methods

### Name(System.String)
Sets the series title displayed in the legend.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Name("Sales"))
        %>

#### Parameters

##### text `System.String`
The title.