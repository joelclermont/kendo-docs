---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### MajorGridLines(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets color and width of the major grid lines and enables them.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MajorGridLines(2, "red", ChartDashType.Dot)
        )
        %>

#### Parameters

##### color `System.Int32`
The major gridlines width

##### width `System.String`
The major gridlines color (CSS syntax)