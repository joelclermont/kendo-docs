---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the tooltip padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Padding(0, 5, 5, 0)
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The tooltip top padding.

##### right `System.Int32`
The tooltip right padding.

##### bottom `System.Int32`
The tooltip bottom padding.

##### left `System.Int32`
The tooltip left padding.