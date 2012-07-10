---
title:ChartAreaLineBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartarealinebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder

Defines the fluent interface for configuring ChartLine.

## Methods

### Color(System.String)
Sets the line color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Color("#f00"))
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The line color (CSS format).

### Width(System.Int32)
Sets the line width

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Width(6))
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The line width.

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the line dashType.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.DashType(ChartDashType.Dot))
        )
        .Render();
        %>

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dashType.

### Opacity(System.Double)
Sets the line opacity.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Opacity(0.2))
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`
The line opacity.