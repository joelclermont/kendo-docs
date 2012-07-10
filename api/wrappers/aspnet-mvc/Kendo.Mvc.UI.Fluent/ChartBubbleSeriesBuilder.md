---
title:ChartBubbleSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbubbleseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBubbleSeriesBuilder

Defines the fluent interface for configuring bubble series.

## Methods

### NegativeValues(System.Action{Kendo.Mvc.UI.Fluent.ChartNegativeValueSettingsBuilder})
Configures the bubble chart behavior for negative values.
            By default negative values are not visible.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bubble(s => s.x, s => s.y, s => s.size)
        .NegativeValues(n => n
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartNegativeValueSettingsBuilder}`
The configuration action.

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

### Markers(System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder})
Not applicable to bubble series

### Markers(System.Boolean)
Not applicable to bubble series