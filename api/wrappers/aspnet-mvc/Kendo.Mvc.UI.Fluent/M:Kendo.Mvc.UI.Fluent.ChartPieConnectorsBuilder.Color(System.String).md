---
title:Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieconnectorsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder

## Methods

### Color(System.String)
Sets the connectors color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(p => p.Sales)
        .Connectors(c => c
        .Color(red)
        );
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The connectors color.