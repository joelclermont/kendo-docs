---
title:Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase

## Methods

### Markers(System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder})
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

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder}`
The configuration action.