---
title:Kendo.Mvc.UI.Fluent.ChartDateCategoryAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdatecategoryaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateCategoryAxisBuilder

## Methods

### AxisCrossingValue(System.Double)
Sets value at which the first perpendicular axis crosses this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis.Date().AxisCrossingValue(4))
        .ValueAxis(axis => axis.Numeric().Title("Axis 1"))
        .ValueAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

#### Parameters

##### axisCrossingValue `System.Double`
The value at which the first perpendicular axis crosses this axis.