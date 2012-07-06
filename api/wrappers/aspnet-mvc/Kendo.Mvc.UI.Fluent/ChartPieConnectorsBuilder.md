---
title:Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieconnectorsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder

## Methods

### Padding(System.Int32)
Sets the connectors padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(p => p.Sales)
        .Connectors(c => c
        .Padding(10)
        );
        )
        .Render();
        %>

#### Parameters

##### padding `System.Int32`
The connectors padding.