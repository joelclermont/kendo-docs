---
title:ChartSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase

Defines the fluent interface for configuring series.

## Properties

### Series
Gets or sets the series.

## Methods

### Name(System.String)
Sets the series title displayed in the legend.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Name("Sales"))
        %>

#### Parameters

##### text `System.String`
The title.

### GroupNameTemplate(System.String)
Sets the name template for auto-generated series when binding to grouped data.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .DataSource(dataSource => dataSource
        .Read(read => read.Action("_StockData", "Scatter_Charts"))
        .Group(group => group.Add(model => model.Symbol)))
        )
        .Series(series => series.Bar(s => s.Sales)
        .Name("Sales")
        .GroupNameTemplate("#= series.name # for #= group.field # #= group.value #")
        )
        .Render();
        %>

#### Parameters

##### groupNameTemplate `System.String`
The name template for auto-generated series when binding to grouped data.

### Opacity(System.Double)
Sets the series opacity.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Opacity(0.5))
        %>

#### Parameters

##### opacity `System.Double`
The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.

### Color(System.String)
Sets the bar fill color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Color("Red"))
        .Render();
        %>

#### Parameters

##### color `System.String`
The bar fill color (CSS syntax).

### Tooltip(System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder})
Configure the data point tooltip for the series.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales)
        .Tooltip(tooltip =>
        {
        tooltip.Visible(true).Format("{0:C}");
        })
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder}`
Use the configurator to set data tooltip options.

### Tooltip(System.Boolean)
Sets the data point tooltip visibility.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Tooltip(true))
        %>

#### Parameters

##### visible `System.Boolean`
A value indicating if the data point tooltip should be displayed.
            The tooltip is not visible by default.

### Axis(System.String)
Sets the axis name to use for this series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Name("Sales").Axis("secondary"))
        .ValueAxis(axis => axis.Numeric())
        .ValueAxis(axis => axis.Numeric("secondary"))
        .CategoryAxis(axis => axis.AxisCrossingValue(0, 10))
        %>

#### Parameters

##### axis `System.String`
The axis name for this series.