---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Color(System.String)
Sets the tooltip text color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Color("Red")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### color `System.String`

            The tooltip text color.
            The default is the same as the series labels color.
            