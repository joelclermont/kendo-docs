---
title:Kendo.Mvc.UI.Fluent.ChartBorderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartborderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBorderBuilder

## Methods

### Color(System.String)
Sets the border color.

#### Parameters

##### color `System.String`
The border color (CSS format).

#### Parameters

##### color `System.String`
The border color (CSS format).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.Color("#f00")))
        .Render();
        %>

### Opacity(System.Double)
Sets the border opacity

#### Parameters

##### opacity `System.Double`
The border opacity (CSS format).

#### Parameters

##### opacity `System.Double`
The border opacity (CSS format).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.Opacity(0.2)))
        .Render();
        %>

### Width(System.Int32)
Sets the border width.

#### Parameters

##### width `System.Int32`
The border width.

#### Parameters

##### width `System.Int32`
The border width.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.Width(2)))
        .Render();
        %>

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the border dashType.

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dashType.

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dashType.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.DashType(ChartDashType.Dot)))
        .Render();
        %>