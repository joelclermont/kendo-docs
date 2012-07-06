---
title:Kendo.Mvc.UI.Fluent.ChartScatterLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterLineSeriesBuilder

## Methods

### MissingValues(Kendo.Mvc.UI.ChartScatterLineMissingValues)
Configures the behavior for handling missing values in scatter line series.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .ScatterLine(s => s.x, s => s.y)
        .MissingValues(ChartScatterLineMissingValues.Interpolate);
        )
        %>

#### Parameters

##### missingValues `Kendo.Mvc.UI.ChartScatterLineMissingValues`
The missing values behavior. The default is to leave gaps.