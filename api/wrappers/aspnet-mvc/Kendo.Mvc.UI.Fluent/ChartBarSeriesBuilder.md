---
title:Kendo.Mvc.UI.Fluent.ChartBarSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbarseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBarSeriesBuilder

## Methods

### Overlay(Kendo.Mvc.UI.ChartBarSeriesOverlay)
Sets the bar effects overlay

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Overlay(ChartBarSeriesOverlay.None))
        .Render();
        %>

#### Parameters

##### overlay `Kendo.Mvc.UI.ChartBarSeriesOverlay`
The bar effects overlay. The default is ChartBarSeriesOverlay.Glass