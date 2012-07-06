---
title:Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartcategoryaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder

## Methods

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