---
title:Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareaseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder

## Methods

### Line(System.Action{Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder})
Configures the area chart line.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Opacity(0.2))
        )
        .Render();
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder}`
The configuration action.