---
title:Kendo.Mvc.UI.Fluent.ChartMarkersBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartmarkersbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartMarkersBuilder

## Methods

### Visible(System.Boolean)
Sets the markers visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The markers visibility.