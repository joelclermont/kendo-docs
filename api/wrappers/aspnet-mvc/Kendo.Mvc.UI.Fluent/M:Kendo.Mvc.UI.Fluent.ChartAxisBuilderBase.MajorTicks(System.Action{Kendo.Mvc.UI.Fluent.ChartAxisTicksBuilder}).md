---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### MajorTicks(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder})
Configures the major ticks.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(axis => axis
        .MajorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder}`
The configuration action.