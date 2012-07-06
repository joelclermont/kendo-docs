---
title:Kendo.Mvc.UI.Fluent.ChartAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaBuilder

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the chart area border.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The border width.

##### color `System.String`
The border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dash type.