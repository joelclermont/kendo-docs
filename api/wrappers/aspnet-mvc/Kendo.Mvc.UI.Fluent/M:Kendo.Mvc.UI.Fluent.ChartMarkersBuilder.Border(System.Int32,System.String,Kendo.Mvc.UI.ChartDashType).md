---
title:Kendo.Mvc.UI.Fluent.ChartMarkersBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartmarkersbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartMarkersBuilder

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the markers border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Border(1, "Red", ChartDashType.Dot)
        );
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The markers border width.

##### color `System.String`
The markers border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The markers border dash type.