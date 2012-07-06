---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### CategoryAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder{`0}})
Configures the category axis

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder{`0}}`
The configurator