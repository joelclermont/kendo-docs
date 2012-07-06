---
title:Kendo.Mvc.UI.Fluent.ChartLegendBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlegendbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLegendBuilder

Defines the fluent interface for configuring the .

## Methods

### Font(System.String)
Sets the legend labels font

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Font("16px Arial,Helvetica,sans-serif"))
        .Render();
        %>

#### Parameters

##### font `System.String`
The legend labels font (CSS format).

### Color(System.String)
Sets the legend labels color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Color("red"))
        .Render();
        %>

#### Parameters

##### color `System.String`
The labels color (CSS format).

### Background(System.String)
Sets the legend background color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Background("red"))
        .Render();
        %>

#### Parameters

##### background `System.String`
The background color.

### Position(Kendo.Mvc.UI.ChartLegendPosition)
Sets the legend position

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Position(ChartLegendPosition.Bottom))
        .Render();
        %>

#### Parameters

##### position `Kendo.Mvc.UI.ChartLegendPosition`
The legend position.

### Visible(System.Boolean)
Sets the legend visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Visible(false))
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The legend visibility.

### Offset(System.Int32,System.Int32)
Sets the legend X and Y offset from its position

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Offset(10, 50))
        .Render();
        %>

#### Parameters

##### offsetX `System.Int32`
The legend X offset from its position.

##### offsetY `System.Int32`
The legend Y offset from its position.

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the legend margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Margin(0, 5, 5, 0))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The legend top margin.

##### right `System.Int32`
The legend right margin.

##### bottom `System.Int32`
The legend bottom margin.

##### left `System.Int32`
The legend top margin.

### Margin(System.Int32)
Sets the legend margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Margin(20))
        .Render();
        %>

#### Parameters

##### margin `System.Int32`
The legend margin.

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the legend padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Padding(0, 5, 5, 0))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The legend top padding.

##### right `System.Int32`
The legend right padding.

##### bottom `System.Int32`
The legend bottom padding.

##### left `System.Int32`
The legend left padding.

### Padding(System.Int32)
Sets the legend padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Padding(20))
        .Render();
        %>

#### Parameters

##### padding `System.Int32`
The legend padding.

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the legend border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The legend border width.

##### color `System.String`
The legend border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The legend border dash type.