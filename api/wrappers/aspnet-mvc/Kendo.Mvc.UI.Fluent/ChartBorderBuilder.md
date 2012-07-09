---
title:Kendo.Mvc.UI.Fluent.ChartBorderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartborderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBorderBuilder

Defines the fluent interface for configuring ChartElementBorder.

## Methods

### Color(System.String)
Sets the border color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.Color("#f00")))
        .Render();
        %>

#### Parameters

##### color `System.String`
The border color (CSS format).

### Opacity(System.Double)
Sets the border opacity

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.Opacity(0.2)))
        .Render();
        %>

#### Parameters

##### opacity `System.Double`
The border opacity (CSS format).

### Width(System.Int32)
Sets the border width.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.Width(2)))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The border width.

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the border dashType.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.DashType(ChartDashType.Dot)))
        .Render();
        %>

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dashType.