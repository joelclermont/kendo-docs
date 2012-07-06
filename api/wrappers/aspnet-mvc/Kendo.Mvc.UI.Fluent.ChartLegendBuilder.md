---
title:Kendo.Mvc.UI.Fluent.ChartLegendBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlegendbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLegendBuilder

## Methods

### Font(System.String)
Sets the legend labels font

#### Parameters

##### font `System.String`
The legend labels font (CSS format).

#### Parameters

##### font `System.String`
The legend labels font (CSS format).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Font("16px Arial,Helvetica,sans-serif"))
        .Render();
        %>

### Color(System.String)
Sets the legend labels color

#### Parameters

##### color `System.String`
The labels color (CSS format).

#### Parameters

##### color `System.String`
The labels color (CSS format).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Color("red"))
        .Render();
        %>

### Background(System.String)
Sets the legend background color

#### Parameters

##### background `System.String`
The background color.

#### Parameters

##### background `System.String`
The background color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Background("red"))
        .Render();
        %>

### Position(Kendo.Mvc.UI.ChartLegendPosition)
Sets the legend position

#### Parameters

##### position `Kendo.Mvc.UI.ChartLegendPosition`
The legend position.

#### Parameters

##### position `Kendo.Mvc.UI.ChartLegendPosition`
The legend position.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Position(ChartLegendPosition.Bottom))
        .Render();
        %>

### Visible(System.Boolean)
Sets the legend visibility

#### Parameters

##### visible `System.Boolean`
The legend visibility.

#### Parameters

##### visible `System.Boolean`
The legend visibility.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Visible(false))
        .Render();
        %>

### Offset(System.Int32,System.Int32)
Sets the legend X and Y offset from its position

#### Parameters

##### offsetX `System.Int32`
The legend X offset from its position.

##### offsetY `System.Int32`
The legend Y offset from its position.

#### Parameters

##### offsetX `System.Int32`
The legend X offset from its position.

##### offsetY `System.Int32`
The legend Y offset from its position.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Offset(10, 50))
        .Render();
        %>

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the legend margin

#### Parameters

##### top `System.Int32`
The legend top margin.

##### right `System.Int32`
The legend right margin.

##### bottom `System.Int32`
The legend bottom margin.

##### left `System.Int32`
The legend top margin.

#### Parameters

##### top `System.Int32`
The legend top margin.

##### right `System.Int32`
The legend right margin.

##### bottom `System.Int32`
The legend bottom margin.

##### left `System.Int32`
The legend top margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Margin(0, 5, 5, 0))
        .Render();
        %>

### Margin(System.Int32)
Sets the legend margin

#### Parameters

##### margin `System.Int32`
The legend margin.

#### Parameters

##### margin `System.Int32`
The legend margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Margin(20))
        .Render();
        %>

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the legend padding

#### Parameters

##### top `System.Int32`
The legend top padding.

##### right `System.Int32`
The legend right padding.

##### bottom `System.Int32`
The legend bottom padding.

##### left `System.Int32`
The legend left padding.

#### Parameters

##### top `System.Int32`
The legend top padding.

##### right `System.Int32`
The legend right padding.

##### bottom `System.Int32`
The legend bottom padding.

##### left `System.Int32`
The legend left padding.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Padding(0, 5, 5, 0))
        .Render();
        %>

### Padding(System.Int32)
Sets the legend padding

#### Parameters

##### padding `System.Int32`
The legend padding.

#### Parameters

##### padding `System.Int32`
The legend padding.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Padding(20))
        .Render();
        %>

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the legend border

#### Parameters

##### width `System.Int32`
The legend border width.

##### color `System.String`
The legend border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The legend border dash type.

#### Parameters

##### width `System.Int32`
The legend border width.

##### color `System.String`
The legend border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The legend border dash type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>