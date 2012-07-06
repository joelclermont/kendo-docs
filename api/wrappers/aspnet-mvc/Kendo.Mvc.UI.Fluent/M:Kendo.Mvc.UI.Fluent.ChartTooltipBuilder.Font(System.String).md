---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Font(System.String)
Sets the tooltip font

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Font("14px Arial,Helvetica,sans-serif")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### font `System.String`
The tooltip font (CSS format).