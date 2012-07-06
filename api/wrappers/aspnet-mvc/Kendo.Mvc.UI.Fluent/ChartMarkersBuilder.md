---
title:Kendo.Mvc.UI.Fluent.ChartMarkersBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartmarkersbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartMarkersBuilder

## Methods

### Background(System.String)
The background color of the current series markers.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Background("Red");
        );
        )
        .Render();
        %>

#### Parameters

##### backgorund `System.String`
The background color of the current series markers. The background color is series color.