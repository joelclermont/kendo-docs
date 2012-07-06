---
title:Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase

## Methods

### Opacity(System.Double)
Sets the series opacity.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Opacity(0.5))
        %>

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            