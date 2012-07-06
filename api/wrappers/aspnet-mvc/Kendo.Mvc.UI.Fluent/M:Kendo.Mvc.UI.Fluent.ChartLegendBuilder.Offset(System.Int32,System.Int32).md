---
title:Kendo.Mvc.UI.Fluent.ChartLegendBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlegendbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLegendBuilder

## Methods

### Offset(System.Int32,System.Int32)
Sets the legend X and Y offset from its position

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Offset(10, 50))
        .Render();
        %>

#### Parameters

##### offsetX `System.Int32`
The legend X offset from its position.

##### offsetY `System.Int32`
The legend Y offset from its position.