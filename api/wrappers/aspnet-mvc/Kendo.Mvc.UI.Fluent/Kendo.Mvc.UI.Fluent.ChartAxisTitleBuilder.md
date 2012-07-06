---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Text(System.String)
Sets the axis title text.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Text("Axis")
        );
        )
        .Render();
        %>

#### Parameters

##### text `System.String`
The text of the axis title.

### Font(System.String)
Sets the axis title font.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Font("16px Arial,Helvetica,sans-serif")
        );
        )
        .Render();
        %>

#### Parameters

##### font `System.String`
The axis title font (CSS format).

### Background(System.String)
Sets the axis title background color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Background("red")
        );
        )
        .Render();
        %>

#### Parameters

##### background `System.String`
The axis background color.

### Color(System.String)
Sets the axis title text color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Color("red")
        );
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The axis text color.

### Position(Kendo.Mvc.UI.ChartAxisTitlePosition)
Sets the axis title position.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Position(ChartTitlePosition.Center)
        );
        )
        .Render();
        %>

#### Parameters

##### position `Kendo.Mvc.UI.ChartAxisTitlePosition`
The axis title position.

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the axis title margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Margin(20, 20, 20, 20)
        );
        )
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The axis title top margin.

##### right `System.Int32`
The axis title right margin.

##### bottom `System.Int32`
The axis title bottom margin.

##### left `System.Int32`
The axis title left margin.

### Margin(System.Int32)
Sets the axis title margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Margin(20)
        );
        )
        .Render();
        %>

#### Parameters

##### margin `System.Int32`
The axis title margin.

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the axis title padding.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Padding(20, 20, 20, 20)
        );
        )
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The axis title top padding.

##### right `System.Int32`
The axis title right padding.

##### bottom `System.Int32`
The axis title bottom padding.

##### left `System.Int32`
The axis title left padding.

### Padding(System.Int32)
Sets the axis title padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Padding(20)
        );
        )
        .Render();
        %>

#### Parameters

##### padding `System.Int32`
The axis title padding.

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the axis title border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Border(1, "#000", ChartDashType.Dot)
        );
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The axis title border width.

##### color `System.String`
The axis title border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The axis title dash type.

### Opacity(System.Double)
Sets the axis title opacity.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Opacity(0.5)
        );
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            