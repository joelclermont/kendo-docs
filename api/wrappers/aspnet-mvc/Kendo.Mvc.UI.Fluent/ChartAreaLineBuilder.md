---
title:Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartarealinebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder

## Methods

### Opacity(System.Double)
Sets the line opacity.

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

##### opacity `System.Double`
The line opacity.