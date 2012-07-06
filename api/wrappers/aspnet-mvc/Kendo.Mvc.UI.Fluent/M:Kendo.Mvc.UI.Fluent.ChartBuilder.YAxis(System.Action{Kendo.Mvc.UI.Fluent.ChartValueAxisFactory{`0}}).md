---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### YAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}})
Configures Y-axis options for scatter charts.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .YAxis(a => a.Numeric().Max(4))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator