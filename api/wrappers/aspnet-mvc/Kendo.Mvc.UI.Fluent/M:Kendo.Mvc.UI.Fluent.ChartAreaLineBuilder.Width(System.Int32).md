---
title:Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartarealinebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder

## Methods

### Width(System.Int32)
Sets the line width

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Width(6))
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The line width.