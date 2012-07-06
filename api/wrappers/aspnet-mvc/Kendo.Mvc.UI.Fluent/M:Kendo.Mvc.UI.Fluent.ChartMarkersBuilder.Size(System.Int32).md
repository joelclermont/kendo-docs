---
title:Kendo.Mvc.UI.Fluent.ChartMarkersBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartmarkersbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartMarkersBuilder

## Methods

### Size(System.Int32)
Sets the markers size.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Size(10)
        );
        )
        .Render();
        %>

#### Parameters

##### size `System.Int32`
The markers size.