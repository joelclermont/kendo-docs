---
title:Kendo.Mvc.UI.Fluent.PlotAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.plotareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PlotAreaBuilder

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the Plot area border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The border width.

##### color `System.String`
The border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dash type.