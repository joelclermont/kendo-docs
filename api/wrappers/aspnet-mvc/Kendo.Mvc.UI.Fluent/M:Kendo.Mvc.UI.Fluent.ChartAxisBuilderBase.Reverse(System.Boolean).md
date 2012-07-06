---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### Reverse(System.Boolean)
Sets the axis reverse option.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Reverse(true)
        )
        %>

#### Parameters

##### reverse `System.Boolean`
A value indicating if the axis labels should be rendered in reverse.