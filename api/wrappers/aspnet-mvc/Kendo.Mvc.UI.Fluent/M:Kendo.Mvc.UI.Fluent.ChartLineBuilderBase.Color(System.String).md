---
title:Kendo.Mvc.UI.Fluent.ChartLineBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlinebuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineBuilderBase

## Methods

### Color(System.String)
Sets the line color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis.MajorGridLines(lines => lines.Color("#f00")))
        .Render();
        %>

#### Parameters

##### color `System.String`
The line color (CSS format).