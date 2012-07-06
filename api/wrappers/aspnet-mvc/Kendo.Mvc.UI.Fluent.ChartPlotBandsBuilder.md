---
title:Kendo.Mvc.UI.Fluent.ChartPlotBandsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartplotbandsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPlotBandsBuilder

## Methods

### 1.From(`0)
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

### 1.To(`0)
Sets the plot band end position.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .PlotBands(plotBands => plotBands
        .Add().To(2).Color("Red");
        )
        )
        .Render();
        %>

#### Parameters

##### to ``0`
The plot band end position.

### 1.Color(System.String)
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

### 1.Opacity(System.Double)
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