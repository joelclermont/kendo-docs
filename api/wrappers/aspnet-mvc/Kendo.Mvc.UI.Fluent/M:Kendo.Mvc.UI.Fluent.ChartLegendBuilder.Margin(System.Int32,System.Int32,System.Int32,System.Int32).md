---
title:Kendo.Mvc.UI.Fluent.ChartLegendBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlegendbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLegendBuilder

## Methods

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the legend margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Margin(0, 5, 5, 0))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The legend top margin.

##### right `System.Int32`
The legend right margin.

##### bottom `System.Int32`
The legend bottom margin.

##### left `System.Int32`
The legend top margin.