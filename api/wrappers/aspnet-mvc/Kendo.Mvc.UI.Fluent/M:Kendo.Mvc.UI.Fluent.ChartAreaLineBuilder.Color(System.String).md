---
title:Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartarealinebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder

## Methods

### Color(System.String)
Sets the line color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Color("#f00"))
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The line color (CSS format).