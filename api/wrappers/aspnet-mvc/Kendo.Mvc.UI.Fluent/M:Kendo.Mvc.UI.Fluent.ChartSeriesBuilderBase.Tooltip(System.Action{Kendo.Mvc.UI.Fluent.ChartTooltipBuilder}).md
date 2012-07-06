---
title:Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase

## Methods

### Tooltip(System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder})
Configure the data point tooltip for the series.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales)
        .Tooltip(tooltip =>
        {
        tooltip.Visible(true).Format("{0:C}");
        })
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder}`
Use the configurator to set data tooltip options.