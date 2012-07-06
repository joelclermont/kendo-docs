---
title:Kendo.Mvc.UI.Fluent.ChartScatterLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterLineSeriesBuilder

## Methods

### 1.Width(System.Double)
Sets the chart line width.

#### Parameters

##### width `System.Double`
The line width.

#### Parameters

##### width `System.Double`
The line width.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.ScatterLine(s => s.x, s => s.y).Width(2))
        .Render();
        %>

### 1.DashType(Kendo.Mvc.UI.ChartDashType)
Sets the chart line dash type.

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dash type.

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dash type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.ScatterLine(s => s.x, s => s.y).DashType(ChartDashType.Dot))
        .Render();
        %>

### 1.MissingValues(Kendo.Mvc.UI.ChartScatterLineMissingValues)
Configures the behavior for handling missing values in scatter line series.

#### Parameters

##### missingValues `Kendo.Mvc.UI.ChartScatterLineMissingValues`
The missing values behavior. The default is to leave gaps.

#### Parameters

##### missingValues `Kendo.Mvc.UI.ChartScatterLineMissingValues`
The missing values behavior. The default is to leave gaps.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .ScatterLine(s => s.x, s => s.y)
        .MissingValues(ChartScatterLineMissingValues.Interpolate);
        )
        %>