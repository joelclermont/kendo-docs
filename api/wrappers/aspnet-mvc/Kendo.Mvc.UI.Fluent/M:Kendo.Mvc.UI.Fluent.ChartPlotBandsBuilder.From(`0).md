---
title:Kendo.Mvc.UI.Fluent.ChartPlotBandsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartplotbandsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPlotBandsBuilder

## Methods

### From(`0)
Sets the plot band start position.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .PlotBands(plotBands => plotBands
        .Add().From(1).Color("Red");
        )
        )
        .Render();
        %>

#### Parameters

##### from ``0`
The plot band start position.