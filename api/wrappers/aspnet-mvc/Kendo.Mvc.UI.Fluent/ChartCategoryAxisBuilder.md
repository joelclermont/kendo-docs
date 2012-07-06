---
title:Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartcategoryaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder

Configures the category axis for the .

## Methods

### Categories``1(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Defines bound categories.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
The expression used to extract the categories value from the chart model

### Categories(System.Collections.IEnumerable)
Defines categories.

#### Parameters

##### categories `System.Collections.IEnumerable`
The list of categories

### Categories(System.String[])
Defines categories.

#### Parameters

##### categories `System.String[]`
The list of categories

### AxisCrossingValue(System.Double)
Sets value at which the first perpendicular axis crosses this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis.AxisCrossingValue(4))
        .ValueAxis(axis => axis.Numeric().Title("Axis 1"))
        .ValueAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

#### Parameters

##### axisCrossingValue `System.Double`
The value at which the first perpendicular axis crosses this axis.

### AxisCrossingValue(System.Double[])
Sets value at which perpendicular axes cross this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis.AxisCrossingValue(0, 10))
        .ValueAxis(axis => axis.Numeric().Title("Axis 1"))
        .ValueAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

#### Parameters

##### axisCrossingValues `System.Double[]`
The values at which perpendicular axes cross this axis.

### AxisCrossingValue(System.Collections.Generic.IEnumerable{System.Double})
Sets value at which perpendicular axes cross this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis.AxisCrossingValue(new double[] { 0, 10 }))
        .ValueAxis(axis => axis.Numeric().Title("Axis 1"))
        .ValueAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

#### Parameters

##### axisCrossingValues `System.Collections.Generic.IEnumerable{System.Double}`
The values at which perpendicular axes cross this axis.