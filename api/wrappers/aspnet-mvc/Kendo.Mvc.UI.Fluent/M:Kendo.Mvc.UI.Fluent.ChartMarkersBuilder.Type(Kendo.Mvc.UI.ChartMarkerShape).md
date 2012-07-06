---
title:Kendo.Mvc.UI.Fluent.ChartMarkersBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartmarkersbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartMarkersBuilder

## Methods

### Type(Kendo.Mvc.UI.ChartMarkerShape)
Sets the markers shape type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Type(ChartMarkerShape.Triangle)
        );
        )
        .Render();
        %>

#### Parameters

##### type `Kendo.Mvc.UI.ChartMarkerShape`
The markers shape type.