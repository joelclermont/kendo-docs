---
title:Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareaseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder

## Methods

### 1.Stack(System.Boolean)
Sets a value indicating if the areas should be stacked.

#### Parameters

##### stacked `System.Boolean`
A value indicating if the areas should be stacked.

#### Parameters

##### stacked `System.Boolean`
A value indicating if the areas should be stacked.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Area(s => s.Sales).Stack(true))
        %>

### 1.Aggregate(Kendo.Mvc.UI.ChartSeriesAggregate)
Sets the aggregate function for date series.
            This function is used when a category (an year, month, etc.) contains two or more points.

#### Parameters

##### aggregate `Kendo.Mvc.UI.ChartSeriesAggregate`
Aggregate function name.

#### Parameters

##### aggregate `Kendo.Mvc.UI.ChartSeriesAggregate`
Aggregate function name.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Area(s => s.Sales).Aggregate())
        %>

### 1.Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder})
Configures the area chart labels.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Labels(labels => labels
        .Position(ChartBarLabelsPosition.Above)
        .Visible(true)
        );
        )
        %>

### 1.Labels(System.Boolean)
Sets the visibility of area chart labels.

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Labels(true);
        )
        %>

### 1.Line(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Configures the area chart line.

#### Parameters

##### configurator `System.Int32`
The configuration action.

#### Parameters

##### configurator `System.Int32`
The configuration action.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(2, "red", ChartDashType.Dot)
        )
        .Render();
        %>

### 1.Line(System.Action{Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder})
Configures the area chart line.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder}`
The configuration action.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Opacity(0.2))
        )
        .Render();
        %>

### 1.Markers(System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder})
Configures the area chart markers.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Markers(markers => markers
        .Type(ChartMarkerShape.Triangle)
        );
        )
        %>

### 1.Markers(System.Boolean)
Sets the visibility of area chart markers.

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is true.

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is true.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Markers(true);
        )
        %>

### 1.MissingValues(Kendo.Mvc.UI.ChartAreaMissingValues)
Configures the behavior for handling missing values in area series.

#### Parameters

##### missingValues `Kendo.Mvc.UI.ChartAreaMissingValues`
The missing values behavior. The default is to leave gaps.

#### Parameters

##### missingValues `Kendo.Mvc.UI.ChartAreaMissingValues`
The missing values behavior. The default is to leave gaps.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .MissingValues(ChartAreaMissingValues.Interpolate);
        )
        %>