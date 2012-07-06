---
title:Kendo.Mvc.UI.Fluent.ChartAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaBuilder

## Methods

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the chart area margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Margin(0, 5, 5, 0))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The chart area top margin.

##### right `System.Int32`
The chart area right margin.

##### bottom `System.Int32`
The chart area bottom margin.

##### left `System.Int32`
The chart area left margin.