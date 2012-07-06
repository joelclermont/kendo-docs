---
title:Kendo.Mvc.UI.Fluent.ChartPlotBandsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartplotbandsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPlotBandsBuilder

## Methods

### Opacity(System.Double)
Sets the plot band opacity

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .PlotBands(plotBands => plotBands
        .Add().Opacity(0.5);
        )
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`
The plot band opacity.