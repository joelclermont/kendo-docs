---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Background(System.String)
Sets the tooltip background color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Background("Red")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### background `System.String`

            The tooltip background color.
            The default is determined from the series color.