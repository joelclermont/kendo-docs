---
title:Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder

## Methods

### Markers(System.Boolean)
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