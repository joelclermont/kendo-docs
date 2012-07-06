---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### PlotArea(System.Action{Kendo.Mvc.UI.Fluent.PlotAreaBuilder})
Sets the Plot area.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.margin(20))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.PlotAreaBuilder}`
The Plot area.