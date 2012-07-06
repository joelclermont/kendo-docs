---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### Tooltip(System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder})
Use it to configure the data point tooltip.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip =>
        {
        tooltip.Visible(true).Format("{0:C}");
        })
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder}`
Use the configurator to set data tooltip options.