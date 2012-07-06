---
title:Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareaseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder

## Methods

### Markers(System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder})
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

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder}`
The configuration action.