---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### Line(System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder})
Configures the axis line.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Line(line => line.Color("#f00"))
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.