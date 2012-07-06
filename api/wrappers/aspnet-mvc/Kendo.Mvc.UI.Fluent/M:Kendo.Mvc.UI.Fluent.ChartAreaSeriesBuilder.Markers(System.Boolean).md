---
title:Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareaseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder

## Methods

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