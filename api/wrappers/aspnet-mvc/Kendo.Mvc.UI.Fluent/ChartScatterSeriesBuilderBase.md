---
title:ChartScatterSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase

Defines the fluent interface for configuring scatter series.

## Methods

### Labels(System.Action\<Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder\>)
Configures the scatter chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Scatter(s => s.x, s => s.y)
        .Labels(labels => labels
        .Position(ChartBarLabelsPosition.Above)
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/ChartPointLabelsBuilder)\>
The configuration action.

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

### Markers(System.Action\<Kendo.Mvc.UI.Fluent.ChartMarkersBuilder\>)
Configures the scatter chart markers.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Scatter(s => s.x, s => s.y)
        .Markers(markers => markers
        .Type(ChartMarkerShape.Triangle)
        );
        )
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.ChartMarkersBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/ChartMarkersBuilder)\>
The configuration action.

### Markers(System.Boolean)
Sets the visibility of scatter chart markers.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Scatter(s => s.x, s => s.y)
        .Markers(true);
        )
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is true.

### XAxis(System.String)
Sets the axis name to use for this series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Scatter(s => s.X, s => s.Y).Name("Scatter").XAxis("secondary"))
        .XAxis(axis => axis.Numeric())
        .XAxis(axis => axis.Numeric("secondary"))
        %>

#### Parameters

##### axis `System.String`
The axis name for this series.

### YAxis(System.String)
Sets the axis name to use for this series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Scatter(s => s.Sales).Name("Sales").YAxis("secondary"))
        .YAxis(axis => axis.Numeric())
        .YAxis(axis => axis.Numeric("secondary"))
        %>

#### Parameters

##### axis `System.String`
The axis name for this series.

### Axis(System.String)
Not applicable to scatter series