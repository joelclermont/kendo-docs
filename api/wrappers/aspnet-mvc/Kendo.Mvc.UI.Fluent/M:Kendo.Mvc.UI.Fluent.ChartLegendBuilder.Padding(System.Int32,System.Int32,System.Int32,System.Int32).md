---
title:Kendo.Mvc.UI.Fluent.ChartLegendBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlegendbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLegendBuilder

## Methods

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the legend padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Padding(0, 5, 5, 0))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The legend top padding.

##### right `System.Int32`
The legend right padding.

##### bottom `System.Int32`
The legend bottom padding.

##### left `System.Int32`
The legend left padding.