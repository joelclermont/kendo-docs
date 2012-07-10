---
title:ChartPieConnectorsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieconnectorsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder

Defines the fluent interface for configuring the chart connectors.

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