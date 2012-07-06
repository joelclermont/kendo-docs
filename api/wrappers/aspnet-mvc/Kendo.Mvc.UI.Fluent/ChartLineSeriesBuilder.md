---
title:Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder

## Methods

### MissingValues(Kendo.Mvc.UI.ChartLineMissingValues)
Configures the behavior for handling missing values in line series.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .MissingValues(ChartLineMissingValues.Interpolate);
        )
        %>

#### Parameters

##### missingValues `Kendo.Mvc.UI.ChartLineMissingValues`
The missing values behavior. The default is to leave gaps.