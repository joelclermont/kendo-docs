---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Text(System.String)
Sets the axis title text.

#### Parameters

##### text `System.String`
The text of the axis title.

#### Parameters

##### text `System.String`
The text of the axis title.

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

### Font(System.String)
Sets the axis title font.

#### Parameters

##### font `System.String`
The axis title font (CSS format).

#### Parameters

##### font `System.String`
The axis title font (CSS format).

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

### Background(System.String)
Sets the axis title background color.

#### Parameters

##### background `System.String`
The axis background color.

#### Parameters

##### background `System.String`
The axis background color.

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

### Color(System.String)
Sets the axis title text color.

#### Parameters

##### color `System.String`
The axis text color.

#### Parameters

##### color `System.String`
The axis text color.

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

### Position(Kendo.Mvc.UI.ChartAxisTitlePosition)
Sets the axis title position.

#### Parameters

##### position `Kendo.Mvc.UI.ChartAxisTitlePosition`
The axis title position.

#### Parameters

##### position `Kendo.Mvc.UI.ChartAxisTitlePosition`
The axis title position.

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

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the axis title margin.

#### Parameters

##### top `System.Int32`
The axis title top margin.

##### right `System.Int32`
The axis title right margin.

##### bottom `System.Int32`
The axis title bottom margin.

##### left `System.Int32`
The axis title left margin.

#### Parameters

##### top `System.Int32`
The axis title top margin.

##### right `System.Int32`
The axis title right margin.

##### bottom `System.Int32`
The axis title bottom margin.

##### left `System.Int32`
The axis title left margin.

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

### Margin(System.Int32)
Sets the axis title margin.

#### Parameters

##### margin `System.Int32`
The axis title margin.

#### Parameters

##### margin `System.Int32`
The axis title margin.

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

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the axis title padding.

#### Parameters

##### top `System.Int32`
The axis title top padding.

##### right `System.Int32`
The axis title right padding.

##### bottom `System.Int32`
The axis title bottom padding.

##### left `System.Int32`
The axis title left padding.

#### Parameters

##### top `System.Int32`
The axis title top padding.

##### right `System.Int32`
The axis title right padding.

##### bottom `System.Int32`
The axis title bottom padding.

##### left `System.Int32`
The axis title left padding.

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

### Padding(System.Int32)
Sets the axis title padding

#### Parameters

##### padding `System.Int32`
The axis title padding.

#### Parameters

##### padding `System.Int32`
The axis title padding.

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

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the axis title border

#### Parameters

##### width `System.Int32`
The axis title border width.

##### color `System.String`
The axis title border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The axis title dash type.

#### Parameters

##### width `System.Int32`
The axis title border width.

##### color `System.String`
The axis title border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The axis title dash type.

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

### Opacity(System.Double)
Sets the axis title opacity.

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

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