---
title:Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareaseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder

## Methods

### MissingValues(Kendo.Mvc.UI.ChartAreaMissingValues)
Configures the behavior for handling missing values in area series.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .MissingValues(ChartAreaMissingValues.Interpolate);
        )
        %>

#### Parameters

##### missingValues `Kendo.Mvc.UI.ChartAreaMissingValues`
The missing values behavior. The default is to leave gaps.