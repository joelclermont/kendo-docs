---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder

## Methods

### BaseUnit(Kendo.Mvc.UI.ChartAxisBaseUnit)
Sets the date axis base unit.

#### Parameters

##### baseUnit `Kendo.Mvc.UI.ChartAxisBaseUnit`

            The date axis base unit
            

#### Parameters

##### baseUnit `Kendo.Mvc.UI.ChartAxisBaseUnit`

            The date axis base unit
            

### Min(System.DateTime)
Sets the start date of the axis.

#### Parameters

##### min `System.DateTime`
The start date of the axis.

#### Parameters

##### min `System.DateTime`
The start date of the axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Date().Min(DateTime.Parse("2012/01/01")))
        %>

### Max(System.DateTime)
Sets the end date of the axis.

#### Parameters

##### max `System.DateTime`
The end date of the axis.

#### Parameters

##### max `System.DateTime`
The end date of the axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Date().Max(DateTime.Parse("2012/01/01")))
        %>

### MajorUnit(System.Double)
Sets the interval between major divisions in base units.

#### Parameters

##### majorUnit `System.Double`
The interval between major divisions in base units.

#### Parameters

##### majorUnit `System.Double`
The interval between major divisions in base units.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Date().BaseUnit(ChartAxisBaseUnit.Months).MajorUnit(4))
        %>

### MinorUnit(System.Double)
Sets the interval between minor divisions in base units.
            It defaults to 1/5th of the majorUnit

#### Parameters

##### majorUnit `System.Double`
The interval between minor divisions in base units.

#### Parameters

##### majorUnit `System.Double`
The interval between minor divisions in base units.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Date().BaseUnit(ChartAxisBaseUnit.Days).MajorUnit(4).MinorUnit(2))
        %>

### AxisCrossingValue(System.DateTime)
Sets value at which the first perpendicular axis crosses this axis.

#### Parameters

##### axisCrossingValue `System.DateTime`
The value at which the first perpendicular axis crosses this axis.

#### Parameters

##### axisCrossingValue `System.DateTime`
The value at which the first perpendicular axis crosses this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(axis => axis.Date().AxisCrossingValue(DateTime.Parse("2012/01/01")))
        %>

### AxisCrossingValue(System.DateTime[])
Sets value at which perpendicular axes cross this axis.

#### Parameters

##### axisCrossingValues `System.DateTime[]`
The values at which perpendicular axes cross this axis.

#### Parameters

##### axisCrossingValues `System.DateTime[]`
The values at which perpendicular axes cross this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis.Date().AxisCrossingValue(DateTime.Parse("2012/01/01"), DateTime.Parse("2012/01/10")))
        .ValueAxis(axis => axis.Numeric().Title("Axis 1"))
        .ValueAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

### AxisCrossingValue(System.Collections.Generic.IEnumerable{System.DateTime})
Sets value at which perpendicular axes cross this axis.

#### Parameters

##### axisCrossingValues `System.Collections.Generic.IEnumerable{System.DateTime}`
The values at which perpendicular axes cross this axis.

#### Parameters

##### axisCrossingValues `System.Collections.Generic.IEnumerable{System.DateTime}`
The values at which perpendicular axes cross this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis.Date().AxisCrossingValue(new DateTime[] {
        DateTime.Parse("2012/01/01"), DateTime.Parse("2012/01/10")
        }))
        .ValueAxis(axis => axis.Numeric().Title("Axis 1"))
        .ValueAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

### Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder})
Configures the axis labels.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .XAxis(axis => axis
        .Date()
        .Labels(labels => labels
        .Culture(new CultureInfo("es-ES")
        .Visible(true)
        );
        )
        %>