---
title:Kendo.Mvc.UI.Fluent.ChartAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaBuilder

## Methods

### Margin(System.Int32)
Sets the chart area margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Margin(5))
        .Render();
        %>

#### Parameters

##### margin `System.Int32`
The chart area margin.