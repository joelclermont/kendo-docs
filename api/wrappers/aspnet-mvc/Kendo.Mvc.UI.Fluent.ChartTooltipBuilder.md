---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Font(System.String)
Sets the tooltip font

#### Parameters

##### font `System.String`
The tooltip font (CSS format).

#### Parameters

##### font `System.String`
The tooltip font (CSS format).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Font("14px Arial,Helvetica,sans-serif")
        .Visible(true)
        )
        .Render();
        %>

### Visible(System.Boolean)
Sets the tooltip visibility

#### Parameters

##### visible `System.Boolean`
The tooltip visibility. The tooltip is not visible by default.

#### Parameters

##### visible `System.Boolean`
The tooltip visibility. The tooltip is not visible by default.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Visible(true)
        )
        .Render();
        %>

### Background(System.String)
Sets the tooltip background color

#### Parameters

##### background `System.String`

            The tooltip background color.
            The default is determined from the series color.

#### Parameters

##### background `System.String`

            The tooltip background color.
            The default is determined from the series color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Background("Red")
        .Visible(true)
        )
        .Render();
        %>

### Color(System.String)
Sets the tooltip text color

#### Parameters

##### color `System.String`

            The tooltip text color.
            The default is the same as the series labels color.
            

#### Parameters

##### color `System.String`

            The tooltip text color.
            The default is the same as the series labels color.
            

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Color("Red")
        .Visible(true)
        )
        .Render();
        %>

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the tooltip padding

#### Parameters

##### top `System.Int32`
The tooltip top padding.

##### right `System.Int32`
The tooltip right padding.

##### bottom `System.Int32`
The tooltip bottom padding.

##### left `System.Int32`
The tooltip left padding.

#### Parameters

##### top `System.Int32`
The tooltip top padding.

##### right `System.Int32`
The tooltip right padding.

##### bottom `System.Int32`
The tooltip bottom padding.

##### left `System.Int32`
The tooltip left padding.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Padding(0, 5, 5, 0)
        .Visible(true)
        )
        .Render();
        %>

### Padding(System.Int32)
Sets the tooltip padding

#### Parameters

##### padding `System.Int32`
The tooltip padding.

#### Parameters

##### padding `System.Int32`
The tooltip padding.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Padding(20)
        .Visible(true)
        )
        .Render();
        %>

### Border(System.Int32,System.String)
Sets the tooltip border

#### Parameters

##### width `System.Int32`
The tooltip border width.

##### color `System.String`
The tooltip border color (CSS syntax).

#### Parameters

##### width `System.Int32`
The tooltip border width.

##### color `System.String`
The tooltip border color (CSS syntax).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Border(1, "Red")
        .Visible(true)
        )
        .Render();
        %>

### Format(System.String)
Sets the tooltip format

#### Parameters

##### format `System.String`
The tooltip format.

#### Parameters

##### format `System.String`
The tooltip format.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Format("{0:C}")
        .Visible(true)
        )
        .Render();
        %>

### Template(System.String)
Sets the tooltip template

#### Parameters

##### template `System.String`
The tooltip template.

#### Parameters

##### template `System.String`
The tooltip template.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Template("<#= category #> - <#= value #>")
        .Visible(true)
        )
        .Render();
        %>

### Opacity(System.Double)
Sets the tooltip opacity.

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
        .Tooltip(tooltip => tooltip
        .Opacity(0.5)
        .Visible(true)
        )
        .Render();
        %>