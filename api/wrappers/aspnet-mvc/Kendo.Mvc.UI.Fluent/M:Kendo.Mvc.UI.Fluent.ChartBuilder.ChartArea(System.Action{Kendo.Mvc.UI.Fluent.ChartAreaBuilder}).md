---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### ChartArea(System.Action{Kendo.Mvc.UI.Fluent.ChartAreaBuilder})
Sets the Chart area.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.margin(20))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAreaBuilder}`
The Chart area.