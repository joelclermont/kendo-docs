---
title:Kendo.Mvc.UI.Fluent.PlotAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.plotareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PlotAreaBuilder

## Methods

### Margin(System.Int32)
Sets the Plot area margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.Margin(5))
        .Render();
        %>

#### Parameters

##### margin `System.Int32`
The plot area margin.