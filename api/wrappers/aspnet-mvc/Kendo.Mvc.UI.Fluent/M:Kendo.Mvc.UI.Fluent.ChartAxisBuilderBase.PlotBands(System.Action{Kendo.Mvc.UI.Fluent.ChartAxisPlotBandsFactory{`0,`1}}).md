---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### PlotBands(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisPlotBandsFactory{`0,`1}})
Defines the plot bands items.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .PlotBands.Add()
        .From(1)
        .To(2)
        )
        %>

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisPlotBandsFactory{`0`
The add action.