---
title:Kendo.Mvc.UI.Fluent.GaugeLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLabelsBuilder

## Methods

### 1.Font(System.String)
Sets the labels font

#### Parameters

##### font `System.String`
The labels font (CSS format).

#### Parameters

##### font `System.String`
The labels font (CSS format).

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Font("14px Arial,Helvetica,sans-serif")
        )
        )
        %>

### 1.Visible(System.Boolean)
Sets the labels visibility

#### Parameters

##### visible `System.Boolean`
The labels visibility.

#### Parameters

##### visible `System.Boolean`
The labels visibility.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Visible(false)
        )
        )
        %>

### 1.Background(System.String)
Sets the labels background color

#### Parameters

##### background `System.String`
The labels background color.

#### Parameters

##### background `System.String`
The labels background color.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Background("Red")
        )
        )
        %>

### 1.Color(System.String)
Sets the labels text color

#### Parameters

##### color `System.String`
The labels text color.

#### Parameters

##### color `System.String`
The labels text color.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Color("Red")
        )
        )
        %>

### 1.Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the labels margin

#### Parameters

##### top `System.Int32`
The labels top margin.

##### right `System.Int32`
The labels right margin.

##### bottom `System.Int32`
The labels bottom margin.

##### left `System.Int32`
The labels left margin.

#### Parameters

##### top `System.Int32`
The labels top margin.

##### right `System.Int32`
The labels right margin.

##### bottom `System.Int32`
The labels bottom margin.

##### left `System.Int32`
The labels left margin.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Margin(0, 5, 5, 0)
        )
        )
        %>els

### 1.Margin(System.Int32)
Sets the labels margin

#### Parameters

##### margin `System.Int32`
The labels margin.

#### Parameters

##### margin `System.Int32`
The labels margin.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Margin(20)
        )
        )
        %>

### 1.Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the labels padding

#### Parameters

##### top `System.Int32`
The labels top padding.

##### right `System.Int32`
The labels right padding.

##### bottom `System.Int32`
The labels bottom padding.

##### left `System.Int32`
The labels left padding.

#### Parameters

##### top `System.Int32`
The labels top padding.

##### right `System.Int32`
The labels right padding.

##### bottom `System.Int32`
The labels bottom padding.

##### left `System.Int32`
The labels left padding.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Padding(0, 5, 5, 0)
        )
        )
        %>

### 1.Padding(System.Int32)
Sets the labels padding

#### Parameters

##### padding `System.Int32`
The labels padding.

#### Parameters

##### padding `System.Int32`
The labels padding.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Padding(20)
        )
        )
        %>

### 1.Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the labels border

#### Parameters

##### width `System.Int32`
The labels border width.

##### color `System.String`
The labels border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The labels border dash type.

#### Parameters

##### width `System.Int32`
The labels border width.

##### color `System.String`
The labels border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The labels border dash type.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Border(1, "Red", ChartDashType.Dot)
        )
        )
        %>

### 1.Format(System.String)
Sets the labels format.

#### Parameters

##### format `System.String`
The labels format.

#### Parameters

##### format `System.String`
The labels format.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Format("{0:C}")
        )
        )
        %>

### 1.Template(System.String)
Sets the labels template.

#### Parameters

##### template `System.String`
The labels template.

#### Parameters

##### template `System.String`
The labels template.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Template("#= value #")
        )
        )
        %>

### 1.Opacity(System.Double)
Sets the labels opacity.

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Opacity(0.5)
        )
        )
        %>