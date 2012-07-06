---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder

## Methods

### AxisCrossingValue(System.Collections.Generic.IEnumerable{System.DateTime})
Sets value at which perpendicular axes cross this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis.Date().AxisCrossingValue(new DateTime[] {
        DateTime.Parse("2012/01/01"), DateTime.Parse("2012/01/10")
        }))
        .ValueAxis(axis => axis.Numeric().Title("Axis 1"))
        .ValueAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

#### Parameters

##### axisCrossingValues `System.Collections.Generic.IEnumerable{System.DateTime}`
The values at which perpendicular axes cross this axis.