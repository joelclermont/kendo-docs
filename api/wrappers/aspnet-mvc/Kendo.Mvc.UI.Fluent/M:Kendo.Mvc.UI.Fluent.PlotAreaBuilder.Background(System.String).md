---
title:Kendo.Mvc.UI.Fluent.PlotAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.plotareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PlotAreaBuilder

## Methods

### Background(System.String)
Sets the Plot area background color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.Background("Red"))
        .Render();
        %>

#### Parameters

##### background `System.String`
The background color.