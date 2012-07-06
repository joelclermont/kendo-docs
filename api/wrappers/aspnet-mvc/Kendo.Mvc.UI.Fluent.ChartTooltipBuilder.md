---
title:Kendo.Mvc.UI.Fluent.ChartTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTooltipBuilder

## Methods

### Font(System.String)
Sets the tooltip font

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Font("14px Arial,Helvetica,sans-serif")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### font `System.String`
The tooltip font (CSS format).

### Visible(System.Boolean)
Sets the tooltip visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The tooltip visibility. The tooltip is not visible by default.

### Background(System.String)
Sets the tooltip background color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Background("Red")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### background `System.String`

            The tooltip background color.
            The default is determined from the series color.

### Color(System.String)
Sets the tooltip text color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Color("Red")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### color `System.String`

            The tooltip text color.
            The default is the same as the series labels color.
            

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the tooltip padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Padding(0, 5, 5, 0)
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The tooltip top padding.

##### right `System.Int32`
The tooltip right padding.

##### bottom `System.Int32`
The tooltip bottom padding.

##### left `System.Int32`
The tooltip left padding.

### Padding(System.Int32)
Sets the tooltip padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Padding(20)
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### padding `System.Int32`
The tooltip padding.

### Border(System.Int32,System.String)
Sets the tooltip border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Border(1, "Red")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The tooltip border width.

##### color `System.String`
The tooltip border color (CSS syntax).

### Format(System.String)
Sets the tooltip format

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Format("{0:C}")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### format `System.String`
The tooltip format.

### Template(System.String)
Sets the tooltip template

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Template("<#= category #> - <#= value #>")
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### template `System.String`
The tooltip template.

### Opacity(System.Double)
Sets the tooltip opacity.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip => tooltip
        .Opacity(0.5)
        .Visible(true)
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            