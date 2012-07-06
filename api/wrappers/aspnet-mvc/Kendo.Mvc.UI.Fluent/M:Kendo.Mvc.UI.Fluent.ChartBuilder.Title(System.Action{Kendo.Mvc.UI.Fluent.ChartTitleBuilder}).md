---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### Title(System.Action{Kendo.Mvc.UI.Fluent.ChartTitleBuilder})
Defines the title of the chart.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Text("Yearly sales"))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTitleBuilder}`
The configuration action.