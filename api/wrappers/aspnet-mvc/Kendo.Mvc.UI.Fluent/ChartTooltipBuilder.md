---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Opacity(System.Double)
Sets the tooltip opacity.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Opacity(0.5)
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            