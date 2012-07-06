---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Border(System.Int32,System.String)
Sets the tooltip border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Border(1, "Red")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The tooltip border width.

##### color `System.String`
The tooltip border color (CSS syntax).