---
title:Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareaseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder

## Methods

### Line(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Configures the area chart line.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(2, "red", ChartDashType.Dot)
        )
        .Render();
        %>

#### Parameters

##### configurator `System.Int32`
The configuration action.