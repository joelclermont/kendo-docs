---
title:Kendo.Mvc.UI.Fluent.ChartBorderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartborderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBorderBuilder

## Methods

### Opacity(System.Double)
Sets the border opacity

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.Opacity(0.2)))
        .Render();
        %>

#### Parameters

##### opacity `System.Double`
The border opacity (CSS format).