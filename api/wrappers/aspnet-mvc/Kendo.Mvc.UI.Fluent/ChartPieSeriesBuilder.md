---
title:Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder

## Methods

### Connectors(System.Action{Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder})
Configures the pie chart connectors.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(s => s.Sales, s => s.DateString)
        .Connectors(c => c
        .Color("red")
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder}`
The configuration action.