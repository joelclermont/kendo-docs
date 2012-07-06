---
title:Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartarealinebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaLineBuilder

## Methods

### Color(System.String)
Sets the line color

#### Parameters

##### color `System.String`
The line color (CSS format).

#### Parameters

##### color `System.String`
The line color (CSS format).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Color("#f00"))
        )
        .Render();
        %>

### Width(System.Int32)
Sets the line width

#### Parameters

##### width `System.Int32`
The line width.

#### Parameters

##### width `System.Int32`
The line width.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Width(6))
        )
        .Render();
        %>

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the line dashType.

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dashType.

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The line dashType.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.DashType(ChartDashType.Dot))
        )
        .Render();
        %>

### Opacity(System.Double)
Sets the line opacity.

#### Parameters

##### opacity `System.Double`
The line opacity.

#### Parameters

##### opacity `System.Double`
The line opacity.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Line(line => line.Opacity(0.2))
        )
        .Render();
        %>