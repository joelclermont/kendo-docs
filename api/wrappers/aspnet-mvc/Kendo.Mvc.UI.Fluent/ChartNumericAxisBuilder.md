---
title:Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartnumericaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder

## Methods

### AxisCrossingValue(System.Collections.Generic.IEnumerable{System.Double})
Sets value at which perpendicular axes cross this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(axis => axis.Numeric().AxisCrossingValue(new double[] { 0, 10 }))
        .YAxis(axis => axis.Numeric().Title("Axis 1"))
        .YAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

#### Parameters

##### axisCrossingValues `System.Collections.Generic.IEnumerable{System.Double}`
The values at which perpendicular axes cross this axis.