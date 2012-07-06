---
title:Kendo.Mvc.UI.Fluent.ChartBubbleSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbubbleseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBubbleSeriesBuilder

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