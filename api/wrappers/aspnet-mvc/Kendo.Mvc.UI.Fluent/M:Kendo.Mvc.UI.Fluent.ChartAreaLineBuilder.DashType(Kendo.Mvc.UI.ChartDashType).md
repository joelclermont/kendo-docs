---
title:Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartarealinebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder

## Methods

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the line dashType.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.DashType(ChartDashType.Dot))
        )
        .Render();
        %>

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dashType.