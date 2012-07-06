---
title:Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder

## Methods

### Markers(System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder})
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