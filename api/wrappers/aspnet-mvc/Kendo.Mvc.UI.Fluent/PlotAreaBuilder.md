---
title:PlotAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.plotareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PlotAreaBuilder

Defines the fluent interface for configuring the PlotArea.

## Methods

### Background(System.String)
Sets the Plot area background color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.Background("Red"))
        .Render();
        %>

#### Parameters

##### background `System.String`
The background color.

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the Plot area margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.Margin(0, 5, 5, 0))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The plot area top margin.

##### right `System.Int32`
The plot area right margin.

##### bottom `System.Int32`
The plot area bottom margin.

##### left `System.Int32`
The plot area left margin.

### Margin(System.Int32)
Sets the Plot area margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.Margin(5))
        .Render();
        %>

#### Parameters

##### margin `System.Int32`
The plot area margin.

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the Plot area border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The border width.

##### color `System.String`
The border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dash type.