---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Template(System.String)
Sets the tooltip template

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Template("<#= category #> - <#= value #>")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### template `System.String`
The tooltip template.