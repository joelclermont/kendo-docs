---
title:ChartScatterLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterLineSeriesBuilder

Defines the fluent interface for configuring scatter line series.

## Methods

### Width(System.Double)
Sets the chart line width.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.ScatterLine(s => s.x, s => s.y).Width(2))
        .Render();
        %>

#### Parameters

##### width `System.Double`
The line width.

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the chart line dash type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.ScatterLine(s => s.x, s => s.y).DashType(ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dash type.

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