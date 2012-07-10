---
title:ChartAreaSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareaseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder

Defines the fluent interface for configuring area series.

## Methods

### Stack(System.Boolean)
Sets a value indicating if the areas should be stacked.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Area(s => s.Sales).Stack(true))
        %>

#### Parameters

##### stacked `System.Boolean`
A value indicating if the areas should be stacked.

### Aggregate(Kendo.Mvc.UI.ChartSeriesAggregate)
Sets the aggregate function for date series.
            This function is used when a category (an year, month, etc.) contains two or more points.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Area(s => s.Sales).Aggregate())
        %>

#### Parameters

##### aggregate `Kendo.Mvc.UI.ChartSeriesAggregate`
Aggregate function name.

### Labels(System.Action\<Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder\>)
Configures the area chart labels.

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

#### Parameters

##### configurator `System.Action<Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder>`
The configuration action.

### Labels(System.Boolean)
Sets the visibility of area chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Labels(true);
        )
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.

### Line(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Configures the area chart line.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(2, "red", ChartDashType.Dot)
        )
        .Render();
        %>

#### Parameters

##### configurator `System.Int32`
The configuration action.

### Line(System.Action\<Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder\>)
Configures the area chart line.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Opacity(0.2))
        )
        .Render();
        %>

#### Parameters

##### configurator `System.Action<Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder>`
The configuration action.

### Markers(System.Action\<Kendo.Mvc.UI.Fluent.ChartMarkersBuilder\>)
Configures the area chart markers.

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

#### Parameters

##### configurator `System.Action<Kendo.Mvc.UI.Fluent.ChartMarkersBuilder>`
The configuration action.

### Markers(System.Boolean)
Sets the visibility of area chart markers.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Markers(true);
        )
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is true.

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