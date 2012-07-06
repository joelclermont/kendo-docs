---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### Series(System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesFactory{`0}})
Defines the chart series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series =>
        {
        series.Bar(s => s.SalesAmount);
        })
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesFactory{`0}}`
The add action.