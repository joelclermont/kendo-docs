---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### MinorTicks(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder})
Configures the minor ticks.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(axis => axis
        .MinorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder}`
The configuration action.