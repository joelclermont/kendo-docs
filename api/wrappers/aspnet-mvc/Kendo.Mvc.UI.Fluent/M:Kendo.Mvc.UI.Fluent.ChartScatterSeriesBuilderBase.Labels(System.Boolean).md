---
title:Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase

## Methods

### Labels(System.Boolean)
Sets the visibility of scatter chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Scatter(s => s.x, s => s.y)
        .Labels(true);
        )
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.