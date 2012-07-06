---
title:Kendo.Mvc.UI.Fluent.ChartLegendBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlegendbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLegendBuilder

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the legend border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The legend border width.

##### color `System.String`
The legend border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The legend border dash type.