---
title:ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

Defines the fluent interface for configuring the ChartTitle.

## Methods

### Text(System.String)
Sets the title text

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Text("Chart"))
        .Render();
        %>

#### Parameters

##### text `System.String`
The text title.

### Font(System.String)
Sets the title font

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Font("16px Arial,Helvetica,sans-serif"))
        .Render();
        %>

#### Parameters

##### font `System.String`
The title font (CSS format).

### Background(System.String)
Sets the title background color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Background("red"))
        .Render();
        %>

#### Parameters

##### background `System.String`
The background color.

### Position(Kendo.Mvc.UI.ChartTitlePosition)
Sets the title position

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Position(ChartTitlePosition.Bottom))
        .Render();
        %>

#### Parameters

##### position `Kendo.Mvc.UI.ChartTitlePosition`
The title position.

### Align(Kendo.Mvc.UI.ChartTextAlignment)
Sets the title alignment

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Align(ChartTextAlignment.Left))
        .Render();
        %>

#### Parameters

##### align `Kendo.Mvc.UI.ChartTextAlignment`
The title alignment.

### Visible(System.Boolean)
Sets the title visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Visible(false))
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The title visibility.

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the title margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Margin(20))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The title top margin.

##### right `System.Int32`
The title right margin.

##### bottom `System.Int32`
The title bottom margin.

##### left `System.Int32`
The title left margin.

### Margin(System.Int32)
Sets the title margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Margin(20))
        .Render();
        %>

#### Parameters

##### margin `System.Int32`
The title margin.

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the title padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Padding(20))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The title top padding.

##### right `System.Int32`
The title right padding.

##### bottom `System.Int32`
The title bottom padding.

##### left `System.Int32`
The title left padding.

### Padding(System.Int32)
Sets the title padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Padding(20))
        .Render();
        %>

#### Parameters

##### padding `System.Int32`
The title padding.

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the title border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The title border width.

##### color `System.String`
The title border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The title dash type.