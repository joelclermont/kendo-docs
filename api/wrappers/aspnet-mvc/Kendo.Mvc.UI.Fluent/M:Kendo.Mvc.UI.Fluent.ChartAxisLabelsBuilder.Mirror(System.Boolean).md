---
title:Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxislabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder

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