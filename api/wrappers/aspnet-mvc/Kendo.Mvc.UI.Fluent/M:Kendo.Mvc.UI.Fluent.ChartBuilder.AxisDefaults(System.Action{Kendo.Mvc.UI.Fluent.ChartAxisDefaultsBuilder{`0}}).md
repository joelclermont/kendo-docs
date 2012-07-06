---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### AxisDefaults(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisDefaultsBuilder{`0}})
Defines the options for all chart axes of the specified type.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .AxisDefaults(axisDefaults => axisDefaults.MinorTickSize(5))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisDefaultsBuilder{`0}}`
The configurator.