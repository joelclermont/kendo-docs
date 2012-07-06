---
title:Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieconnectorsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder

## Methods

### Width(System.Int32)
Sets the connectors width

#### Parameters

##### width `System.Int32`
The connectors width.

#### Parameters

##### width `System.Int32`
The connectors width.

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

### Color(System.String)
Sets the connectors color

#### Parameters

##### color `System.String`
The connectors color.

#### Parameters

##### color `System.String`
The connectors color.

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

### Padding(System.Int32)
Sets the connectors padding

#### Parameters

##### padding `System.Int32`
The connectors padding.

#### Parameters

##### padding `System.Int32`
The connectors padding.

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