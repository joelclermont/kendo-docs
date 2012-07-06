---
title:Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlabelsbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase

## Methods

### 1.Font(System.String)
Sets the labels font

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Font("14px Arial,Helvetica,sans-serif")
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### font `System.String`
The labels font (CSS format).

### 1.Visible(System.Boolean)
Sets the labels visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The labels visibility.

### 1.Background(System.String)
Sets the labels background color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Background("Red")
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### background `System.String`
The labels background color.

### 1.Color(System.String)
Sets the labels text color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Color("Red")
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The labels text color.

### 1.Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the labels margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Margin(0, 5, 5, 0)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The labels top margin.

##### right `System.Int32`
The labels right margin.

##### bottom `System.Int32`
The labels bottom margin.

##### left `System.Int32`
The labels left margin.

### 1.Margin(System.Int32)
Sets the labels margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Margin(20)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### margin `System.Int32`
The labels margin.

### 1.Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the labels padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Padding(0, 5, 5, 0)
        .Visible(true);
        );
        )
        .Render();
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

### 1.Padding(System.Int32)
Sets the labels padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Padding(20)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### padding `System.Int32`
The labels padding.

### 1.Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the labels border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Border(1, "Red", ChartDashType.Dot)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The labels border width.

##### color `System.String`
The labels border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The labels border dash type.

### 1.Format(System.String)
Sets the labels format.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Format("{0:C}")
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### format `System.String`
The labels format.

### 1.Template(System.String)
Sets the labels template.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Template("${TotalSales}")
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### template `System.String`
The labels template.

### 1.Opacity(System.Double)
Sets the labels opacity.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Opacity(0.5)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

### 1.Rotation(System.Int32)
Sets the labels text rotation

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Rotation(45)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### rotation `System.Int32`
The labels text rotation.