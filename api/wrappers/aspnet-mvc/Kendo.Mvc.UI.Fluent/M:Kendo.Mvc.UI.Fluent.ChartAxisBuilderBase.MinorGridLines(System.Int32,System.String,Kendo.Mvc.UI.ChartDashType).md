---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### MinorGridLines(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets color and width of the minor grid lines and enables them.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MinorGridLines(2, "red", ChartDashType.Dot)
        )
        %>

#### Parameters

##### color `System.Int32`
The minor gridlines width

##### width `System.String`
The minor gridlines color (CSS syntax)