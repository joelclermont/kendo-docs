---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### Title(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder})
Configures the chart axis title.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Title(title => title.Text("Axis"))
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder}`
The configuration action.