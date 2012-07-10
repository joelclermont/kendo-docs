---
title:GaugeLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLabelsBuilder

Defines the fluent interface for configuring the gauge labels.

## Methods

### Font(System.String)
Sets the labels font

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Font("14px Arial,Helvetica,sans-serif")
        )
        )
        %>

#### Parameters

##### font `System.String`
The labels font (CSS format).

### Visible(System.Boolean)
Sets the labels visibility

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Visible(false)
        )
        )
        %>

#### Parameters

##### visible `System.Boolean`
The labels visibility.

### Background(System.String)
Sets the labels background color

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Background("Red")
        )
        )
        %>

#### Parameters

##### background `System.String`
The labels background color.

### Color(System.String)
Sets the labels text color

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Color("Red")
        )
        )
        %>

#### Parameters

##### color `System.String`
The labels text color.

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the labels margin

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Margin(0, 5, 5, 0)
        )
        )
        %>els

#### Parameters

##### top `System.Int32`
The labels top margin.

##### right `System.Int32`
The labels right margin.

##### bottom `System.Int32`
The labels bottom margin.

##### left `System.Int32`
The labels left margin.

### Margin(System.Int32)
Sets the labels margin

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Margin(20)
        )
        )
        %>

#### Parameters

##### margin `System.Int32`
The labels margin.

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the labels padding

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Padding(0, 5, 5, 0)
        )
        )
        %>

#### Parameters

##### top `System.Int32`
The labels top padding.

##### right `System.Int32`
The labels right padding.

##### bottom `System.Int32`
The labels bottom padding.

##### left `System.Int32`
The labels left padding.

### Padding(System.Int32)
Sets the labels padding

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Padding(20)
        )
        )
        %>

#### Parameters

##### padding `System.Int32`
The labels padding.

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the labels border

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Border(1, "Red", ChartDashType.Dot)
        )
        )
        %>

#### Parameters

##### width `System.Int32`
The labels border width.

##### color `System.String`
The labels border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The labels border dash type.

### Format(System.String)
Sets the labels format.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Format("{0:C}")
        )
        )
        %>

#### Parameters

##### format `System.String`
The labels format.

### Template(System.String)
Sets the labels template.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Template("#= value #")
        )
        )
        %>

#### Parameters

##### template `System.String`
The labels template.

### Opacity(System.Double)
Sets the labels opacity.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Opacity(0.5)
        )
        )
        %>

#### Parameters

##### opacity `System.Double`
The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.