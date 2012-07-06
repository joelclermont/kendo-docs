---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder

## Methods

### AxisCrossingValue(System.DateTime)
Sets value at which the first perpendicular axis crosses this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(axis => axis.Date().AxisCrossingValue(DateTime.Parse("2012/01/01")))
        %>

#### Parameters

##### axisCrossingValue `System.DateTime`
The value at which the first perpendicular axis crosses this axis.