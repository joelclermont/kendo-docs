---
title:Kendo.Mvc.UI.Fluent.ChartLineBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlinebuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineBuilderBase

## Methods

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the line dashType.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis.MajorGridLines(lines => lines.DashType(ChartDashType.Dot)))
        .Render();
        %>

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dashType.