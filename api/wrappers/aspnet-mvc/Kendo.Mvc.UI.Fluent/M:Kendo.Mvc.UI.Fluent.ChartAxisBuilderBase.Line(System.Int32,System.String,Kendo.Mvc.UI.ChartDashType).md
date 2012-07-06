---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### Line(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets color and width of the lines and enables them.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Line(2, "#f00", ChartDashType.Dot)
        )
        %>

#### Parameters

##### color `System.Int32`
The axis line width

##### width `System.String`
The axis line color (CSS syntax)