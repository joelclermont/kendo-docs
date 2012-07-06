---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Padding(System.Int32)
Sets the tooltip padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Padding(20)
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### padding `System.Int32`
The tooltip padding.