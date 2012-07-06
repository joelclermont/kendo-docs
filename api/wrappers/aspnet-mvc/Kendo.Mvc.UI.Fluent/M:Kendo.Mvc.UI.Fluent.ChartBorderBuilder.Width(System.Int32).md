---
title:Kendo.Mvc.UI.Fluent.ChartBorderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartborderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBorderBuilder

## Methods

### Width(System.Int32)
Sets the border width.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.Width(2)))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The border width.