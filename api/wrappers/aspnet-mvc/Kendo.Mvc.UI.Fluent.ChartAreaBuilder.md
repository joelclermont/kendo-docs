---
title:Kendo.Mvc.UI.Fluent.ChartAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaBuilder

## Methods

### Background(System.String)
Sets the chart area background color.

#### Parameters

##### background `System.String`
The background color.

#### Parameters

##### background `System.String`
The background color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Background("Red"))
        .Render();
        %>

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the chart area margin.

#### Parameters

##### top `System.Int32`
The chart area top margin.

##### right `System.Int32`
The chart area right margin.

##### bottom `System.Int32`
The chart area bottom margin.

##### left `System.Int32`
The chart area left margin.

#### Parameters

##### top `System.Int32`
The chart area top margin.

##### right `System.Int32`
The chart area right margin.

##### bottom `System.Int32`
The chart area bottom margin.

##### left `System.Int32`
The chart area left margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Margin(0, 5, 5, 0))
        .Render();
        %>

### Margin(System.Int32)
Sets the chart area margin.

#### Parameters

##### margin `System.Int32`
The chart area margin.

#### Parameters

##### margin `System.Int32`
The chart area margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Margin(5))
        .Render();
        %>

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the chart area border.

#### Parameters

##### width `System.Int32`
The border width.

##### color `System.String`
The border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dash type.

#### Parameters

##### width `System.Int32`
The border width.

##### color `System.String`
The border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dash type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>