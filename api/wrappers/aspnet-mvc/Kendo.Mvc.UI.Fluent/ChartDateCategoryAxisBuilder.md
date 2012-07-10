---
title:ChartDateCategoryAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdatecategoryaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateCategoryAxisBuilder

Configures date category axis for the !:Chart{TModel}.

## Properties

### Container
The parent Chart

## Methods

### Categories(System.Linq.Expressions.Expression<System.Func<T>,System.DateTime>)
Defines bound categories.

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T>`
The expression used to extract the categories value from the chart model

### Categories(System.Collections.Generic.IEnumerable<System.DateTime>)
Defines categories.

#### Parameters

##### categories `System.Collections.Generic.IEnumerable<System.DateTime>`
The list of categories

### Categories(System.DateTime[])
Defines categories.

#### Parameters

##### categories `System.DateTime[]`
The list of categories

### BaseUnit(Kendo.Mvc.UI.ChartAxisBaseUnit)
Sets the date category axis base unit.

#### Parameters

##### baseUnit [Kendo.Mvc.UI.ChartAxisBaseUnit](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/ChartAxisBaseUnit)
The date category axis base unit

### Min(System.DateTime)
Sets the date category axis minimum (start) date.

#### Parameters

##### min `System.DateTime`
The date category axis minimum (start) date

### Max(System.DateTime)
Sets the date category axis maximum (end) date.

#### Parameters

##### min `System.DateTime`
The date category axis maximum (end) date

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

### AxisCrossingValue(System.Double[])
Sets value at which perpendicular axes cross this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis.Date().AxisCrossingValue(0, 10))
        .ValueAxis(axis => axis.Numeric().Title("Axis 1"))
        .ValueAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

#### Parameters

##### axisCrossingValues `System.Double[]`
The values at which perpendicular axes cross this axis.

### AxisCrossingValue(System.Collections.Generic.IEnumerable<System.Double>)
Sets value at which perpendicular axes cross this axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis.Date().AxisCrossingValue(new double[] { 0, 10 }))
        .ValueAxis(axis => axis.Numeric().Title("Axis 1"))
        .ValueAxis(axis => axis.Numeric("secondary").Title("Axis 2"))
        %>

#### Parameters

##### axisCrossingValues `System.Collections.Generic.IEnumerable<System.Double>`
The values at which perpendicular axes cross this axis.

### Labels(System.Action<Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder>)
Configures the axis labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Date()
        .Labels(labels => labels
        .Culture(new CultureInfo("es-ES")
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator System.Action<[Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder>](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/ChartDateAxisLabelsBuilder>)>
The configuration action.