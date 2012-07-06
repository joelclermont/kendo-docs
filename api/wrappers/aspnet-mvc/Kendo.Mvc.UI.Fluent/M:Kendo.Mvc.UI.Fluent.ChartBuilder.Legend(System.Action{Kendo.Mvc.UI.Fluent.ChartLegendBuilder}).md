---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### Legend(System.Action{Kendo.Mvc.UI.Fluent.ChartLegendBuilder})
Configures the legend.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Visible(true).Position(ChartLegendPosition.Bottom))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLegendBuilder}`
The configuration action.