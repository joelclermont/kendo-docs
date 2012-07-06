---
title:Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase

## Methods

### 2.Name(System.String)
Sets the series title displayed in the legend.

#### Parameters

##### text `System.String`
The title.

#### Parameters

##### text `System.String`
The title.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Name("Sales"))
        %>

### 2.Opacity(System.Double)
Sets the series opacity.

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Opacity(0.5))
        %>

### 2.Color(System.String)
Sets the bar fill color

#### Parameters

##### color `System.String`
The bar fill color (CSS syntax).

#### Parameters

##### color `System.String`
The bar fill color (CSS syntax).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Color("Red"))
        .Render();
        %>

### 2.Tooltip(System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder})
Configure the data point tooltip for the series.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder}`
Use the configurator to set data tooltip options.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder}`
Use the configurator to set data tooltip options.

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

### 2.Tooltip(System.Boolean)
Sets the data point tooltip visibility.

#### Parameters

##### visible `System.Boolean`

            A value indicating if the data point tooltip should be displayed.
            The tooltip is not visible by default.
            

#### Parameters

##### visible `System.Boolean`

            A value indicating if the data point tooltip should be displayed.
            The tooltip is not visible by default.
            

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Tooltip(true))
        %>

### 2.Axis(System.String)
Sets the axis name to use for this series.

#### Parameters

##### axis `System.String`
The axis name for this series.

#### Parameters

##### axis `System.String`
The axis name for this series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Name("Sales").Axis("secondary"))
        .ValueAxis(axis => axis.Numeric())
        .ValueAxis(axis => axis.Numeric("secondary"))
        .CategoryAxis(axis => axis.AxisCrossingValue(0, 10))
        %>