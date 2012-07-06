---
title:Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder

## Methods

### Overlay(Kendo.Mvc.UI.ChartPieSeriesOverlay)
Sets the pie segments effects overlay

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).Overlay(ChartPieSeriesOverlay.None))
        .Render();
        %>

#### Parameters

##### overlay `Kendo.Mvc.UI.ChartPieSeriesOverlay`

            The pie segment effects overlay.
            The default value is set in the theme.
            