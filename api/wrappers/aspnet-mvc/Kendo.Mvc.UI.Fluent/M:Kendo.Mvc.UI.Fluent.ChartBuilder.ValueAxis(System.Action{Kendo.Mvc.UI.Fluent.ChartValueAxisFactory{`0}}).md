---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### ValueAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}})
Defines value axis options

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric().TickSize(4))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator