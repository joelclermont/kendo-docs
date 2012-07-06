---
title:Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxislabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder

Defines the fluent interface for configuring the chart labels.

## Methods

### Mirror(System.Boolean)
Renders the axis labels on the other side.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .ValueAxis(axis => axis
        .Numeric().Labels(labels => labels.Mirror(true))
        )
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        // Move the value axis to the right side
        .AxisCrossingValue(5)
        )
        %>

#### Parameters

##### mirror `System.Boolean`
A value indicating whether to render the axis labels on the other side.

### Step(System.Int32)
Label rendering step.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(product => product.Name)
        .Labels(labels => labels.Step(2))
        )
        %>

#### Parameters

##### step `System.Int32`
A value indicating the step at which labels are rendered.
            Every n-th label is rendered where n is the step.

### Skip(System.Int32)
Label rendering skip.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(product => product.Name)
        .Labels(labels => labels.Skip(2))
        )
        %>

#### Parameters

##### skip `System.Int32`
Skips rendering the first n labels.