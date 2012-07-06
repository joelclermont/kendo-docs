---
title:Kendo.Mvc.UI.Fluent.ChartPlotBandsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartplotbandsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPlotBandsBuilder

## Methods

### Color(System.String)
Sets the plot band background color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .PlotBands(plotBands => plotBands
        .Add().Color("Red");
        )
        )
        .Render();
        %>

#### Parameters

##### background `System.String`
The plot band background color.