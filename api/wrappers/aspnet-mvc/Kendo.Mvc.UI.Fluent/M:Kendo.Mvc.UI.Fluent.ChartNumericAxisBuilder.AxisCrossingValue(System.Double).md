---
title:Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartnumericaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder

## Methods

### AxisCrossingValue(System.Double)
Sets value at which the first perpendicular axis crosses this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(axis => axis.AxisCrossingValue(4))
        %>

#### Parameters

##### axisCrossingValue `System.Double`
The value at which the first perpendicular axis crosses this axis.