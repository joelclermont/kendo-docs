---
title:Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase

## Methods

### Tooltip(System.Boolean)
Sets the data point tooltip visibility.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Tooltip(true))
        %>

#### Parameters

##### visible `System.Boolean`

            A value indicating if the data point tooltip should be displayed.
            The tooltip is not visible by default.
            