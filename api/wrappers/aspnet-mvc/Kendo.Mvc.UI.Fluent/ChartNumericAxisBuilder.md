---
title:ChartNumericAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartnumericaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder

Defines the fluent interface for configuring numeric axis.

## Methods

### Min(System.Double)
Sets the axis minimum value.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric().Min(4))
        %>

#### Parameters

##### min `System.Double`
The axis minimum value.

### Max(System.Double)
Sets the axis maximum value.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric().Max(4))
        %>

#### Parameters

##### max `System.Double`
The axis maximum value.

### MajorUnit(System.Double)
Sets the interval between major divisions.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric().MajorUnit(4))
        %>

#### Parameters

##### majorUnit `System.Double`
The interval between major divisions.

### MinorUnit(System.Double)
Sets the interval between minor divisions.
            It defaults to MajorUnit / 5.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric()
        .MajorUnit(4)
        .MinorUnit(2)
        .MinorTicks(mt => mt.Visible(true))
        )
        %>

#### Parameters

##### minorUnit `System.Double`
The interval between minor divisions.

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

### AxisCrossingValue(System.Double[])
Sets value at which perpendicular axes cross this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(axis => axis.Numeric().AxisCrossingValue(0, 10))
        .YAxis(axis => axis.Numeric().Title("Axis 1"))
        .YAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

#### Parameters

##### axisCrossingValues `System.Double[]`
The values at which perpendicular axes cross this axis.

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