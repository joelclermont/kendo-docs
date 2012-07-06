---
title:Kendo.Mvc.UI.Fluent.PlotAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.plotareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PlotAreaBuilder

## Methods

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the Plot area margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.Margin(0, 5, 5, 0))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The plot area top margin.

##### right `System.Int32`
The plot area right margin.

##### bottom `System.Int32`
The plot area bottom margin.

##### left `System.Int32`
The plot area left margin.