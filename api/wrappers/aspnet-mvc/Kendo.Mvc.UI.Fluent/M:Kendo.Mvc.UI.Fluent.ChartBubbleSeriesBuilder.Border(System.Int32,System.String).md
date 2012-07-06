---
title:Kendo.Mvc.UI.Fluent.ChartBubbleSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbubbleseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBubbleSeriesBuilder

## Methods

### Border(System.Int32,System.String)
Sets the bubble border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bubble(s => s.x, s => s.y, s => s.size)
        .Border(1, "Red");
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The bubble border width.

##### color `System.String`
The bubble border color (CSS syntax).