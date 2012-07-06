---
title:Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieconnectorsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder

## Methods

### Width(System.Int32)
Sets the connectors width

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(p => p.Sales)
        .Connectors(c => c
        .Width(3)
        );
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The connectors width.