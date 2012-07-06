---
title:Kendo.Mvc.UI.Fluent.ChartBubbleSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbubbleseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBubbleSeriesBuilder

## Methods

### 1.NegativeValues(System.Action{Kendo.Mvc.UI.Fluent.ChartNegativeValueSettingsBuilder})
Configures the bubble chart behavior for negative values.
            By default negative values are not visible.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartNegativeValueSettingsBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartNegativeValueSettingsBuilder}`
The configuration action.

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

### 1.Border(System.Int32,System.String)
Sets the bubble border

#### Parameters

##### width `System.Int32`
The bubble border width.

##### color `System.String`
The bubble border color (CSS syntax).

#### Parameters

##### width `System.Int32`
The bubble border width.

##### color `System.String`
The bubble border color (CSS syntax).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bubble(s => s.x, s => s.y, s => s.size)
        .Border(1, "Red");
        )
        .Render();
        %>

### 1.Markers(System.Action{Kendo.Mvc.UI.Fluent.ChartMarkersBuilder})
Not applicable to bubble series

### 1.Markers(System.Boolean)
Not applicable to bubble series