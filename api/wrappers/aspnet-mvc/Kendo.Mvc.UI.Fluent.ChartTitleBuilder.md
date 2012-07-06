---
title:Kendo.Mvc.UI.Fluent.ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

## Methods

### Text(System.String)
Sets the title text

#### Parameters

##### text `System.String`
The text title.

#### Parameters

##### text `System.String`
The text title.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Text("Chart"))
        .Render();
        %>

### Font(System.String)
Sets the title font

#### Parameters

##### font `System.String`
The title font (CSS format).

#### Parameters

##### font `System.String`
The title font (CSS format).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Font("16px Arial,Helvetica,sans-serif"))
        .Render();
        %>

### Background(System.String)
Sets the title background color

#### Parameters

##### background `System.String`
The background color.

#### Parameters

##### background `System.String`
The background color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Background("red"))
        .Render();
        %>

### Position(Kendo.Mvc.UI.ChartTitlePosition)
Sets the title position

#### Parameters

##### position `Kendo.Mvc.UI.ChartTitlePosition`
The title position.

#### Parameters

##### position `Kendo.Mvc.UI.ChartTitlePosition`
The title position.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Position(ChartTitlePosition.Bottom))
        .Render();
        %>

### Align(Kendo.Mvc.UI.ChartTextAlignment)
Sets the title alignment

#### Parameters

##### align `Kendo.Mvc.UI.ChartTextAlignment`
The title alignment.

#### Parameters

##### align `Kendo.Mvc.UI.ChartTextAlignment`
The title alignment.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Align(ChartTextAlignment.Left))
        .Render();
        %>

### Visible(System.Boolean)
Sets the title visibility

#### Parameters

##### visible `System.Boolean`
The title visibility.

#### Parameters

##### visible `System.Boolean`
The title visibility.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Visible(false))
        .Render();
        %>

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the title margin

#### Parameters

##### top `System.Int32`
The title top margin.

##### right `System.Int32`
The title right margin.

##### bottom `System.Int32`
The title bottom margin.

##### left `System.Int32`
The title left margin.

#### Parameters

##### top `System.Int32`
The title top margin.

##### right `System.Int32`
The title right margin.

##### bottom `System.Int32`
The title bottom margin.

##### left `System.Int32`
The title left margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Margin(20))
        .Render();
        %>

### Margin(System.Int32)
Sets the title margin

#### Parameters

##### margin `System.Int32`
The title margin.

#### Parameters

##### margin `System.Int32`
The title margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Margin(20))
        .Render();
        %>

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the title padding

#### Parameters

##### top `System.Int32`
The title top padding.

##### right `System.Int32`
The title right padding.

##### bottom `System.Int32`
The title bottom padding.

##### left `System.Int32`
The title left padding.

#### Parameters

##### top `System.Int32`
The title top padding.

##### right `System.Int32`
The title right padding.

##### bottom `System.Int32`
The title bottom padding.

##### left `System.Int32`
The title left padding.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Padding(20))
        .Render();
        %>

### Padding(System.Int32)
Sets the title padding

#### Parameters

##### padding `System.Int32`
The title padding.

#### Parameters

##### padding `System.Int32`
The title padding.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Padding(20))
        .Render();
        %>

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the title border

#### Parameters

##### width `System.Int32`
The title border width.

##### color `System.String`
The title border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The title dash type.

#### Parameters

##### width `System.Int32`
The title border width.

##### color `System.String`
The title border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The title dash type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>