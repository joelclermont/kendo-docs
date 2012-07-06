---
title:Kendo.Mvc.UI.Fluent.ChartBorderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartborderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBorderBuilder

## Methods

### Color(System.String)
Sets the border color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.Color("#f00")))
        .Render();
        %>

#### Parameters

##### color `System.String`
The border color (CSS format).