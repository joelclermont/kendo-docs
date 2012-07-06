---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Visible(System.Boolean)
Sets the tooltip visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The tooltip visibility. The tooltip is not visible by default.