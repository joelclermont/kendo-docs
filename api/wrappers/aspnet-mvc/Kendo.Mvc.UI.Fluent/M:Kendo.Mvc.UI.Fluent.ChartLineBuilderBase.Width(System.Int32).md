---
title:Kendo.Mvc.UI.Fluent.ChartLineBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlinebuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineBuilderBase

## Methods

### Width(System.Int32)
Sets the line width

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis.MajorGridLines(lines => lines.Width(2)))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The line width.