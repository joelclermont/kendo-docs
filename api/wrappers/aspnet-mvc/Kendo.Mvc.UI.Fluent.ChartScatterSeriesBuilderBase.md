---
title:Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase

## Methods

### 2.Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder})
Configures the scatter chart labels.

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
        .Scatter(s => s.x, s => s.y)
        .Labels(labels => labels
        .Position(ChartBarLabelsPosition.Above)
        .Visible(true)
        );
        )
        %>

### 2.Labels(System.Boolean)
Sets the visibility of scatter chart labels.

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
        .Scatter(s => s.x, s => s.y)
        .Labels(true);
        )
        %>

### 2.Markers(System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder})
Configures the scatter chart markers.

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
        .Scatter(s => s.x, s => s.y)
        .Markers(markers => markers
        .Type(ChartMarkerShape.Triangle)
        );
        )
        %>

### 2.Markers(System.Boolean)
Sets the visibility of scatter chart markers.

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
        .Scatter(s => s.x, s => s.y)
        .Markers(true);
        )
        %>

### 2.XAxis(System.String)
Sets the axis name to use for this series.

#### Parameters

##### axis `System.String`
The axis name for this series.

#### Parameters

##### axis `System.String`
The axis name for this series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Scatter(s => s.X, s => s.Y).Name("Scatter").XAxis("secondary"))
        .XAxis(axis => axis.Numeric())
        .XAxis(axis => axis.Numeric("secondary"))
        %>

### 2.YAxis(System.String)
Sets the axis name to use for this series.

#### Parameters

##### axis `System.String`
The axis name for this series.

#### Parameters

##### axis `System.String`
The axis name for this series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Scatter(s => s.Sales).Name("Sales").YAxis("secondary"))
        .YAxis(axis => axis.Numeric())
        .YAxis(axis => axis.Numeric("secondary"))
        %>

### 2.Axis(System.String)
Not applicable to scatter series