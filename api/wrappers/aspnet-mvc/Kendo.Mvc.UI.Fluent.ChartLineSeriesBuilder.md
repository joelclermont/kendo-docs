---
title:Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder

## Methods

### 1.Stack(System.Boolean)
Sets a value indicating if the lines should be stacked.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Line(s => s.Sales).Stack(true))
        %>

#### Parameters

##### stacked `System.Boolean`
A value indicating if the lines should be stacked.

### 1.Aggregate(Kendo.Mvc.UI.ChartSeriesAggregate)
Sets the aggregate function for date series.
            This function is used when a category (an year, month, etc.) contains two or more points.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Line(s => s.Sales).Aggregate())
        %>

#### Parameters

##### aggregate `Kendo.Mvc.UI.ChartSeriesAggregate`
Aggregate function name.

### 1.Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder})
Configures the line chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Labels(labels => labels
        .Position(ChartBarLabelsPosition.Above)
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder}`
The configuration action.

### 1.Labels(System.Boolean)
Sets the visibility of line chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Labels(true);
        )
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.

### 1.Width(System.Double)
Sets the line chart line width.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Line(s => s.Sales).Width(2))
        .Render();
        %>

#### Parameters

##### width `System.Double`
The line width.

### 1.DashType(Kendo.Mvc.UI.ChartDashType)
Sets the line chart line dash type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Line(s => s.Sales).DashType(ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dash type.

### 1.Markers(System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder})
Configures the line chart markers.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Type(ChartMarkerShape.Triangle)
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder}`
The configuration action.

### 1.Markers(System.Boolean)
Sets the visibility of line chart markers.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(true);
        )
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is true.

### 1.MissingValues(Kendo.Mvc.UI.ChartLineMissingValues)
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