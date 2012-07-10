---
title:ChartPieSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder

Defines the fluent interface for configuring pie series.

## Properties

### Series
Gets or sets the series.

## Methods

### Name(System.String)
Sets the name of the series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).Name("Sales"))
        %>

### Opacity(System.Double)
Sets the series opacity.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).Opacity(0.5))
        %>

#### Parameters

##### opacity `System.Double`
The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.

### Padding(System.Int32)
Sets the padding of the chart.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).Padding(100))
        .Render();
        %>

### StartAngle(System.Int32)
Sets the start angle of the first pie segment.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).StartAngle(100))
        .Render();
        %>

#### Parameters

##### startAngle `System.Int32`
The pie start angle(in degrees).

### Labels(System.Action\<Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder\>)
Configures the pie chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(s => s.Sales, s => s.DateString)
        .Labels(labels => labels
        .Color("red")
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action<Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder>`
The configuration action.

### Labels(System.Boolean)
Sets the visibility of pie chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(s => s.Sales, s => s.DateString)
        .Labels(true);
        )
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the pie segments border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The pie segments border width.

##### color `System.String`
The pie segments border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The pie segments border dash type.

### Overlay(Kendo.Mvc.UI.ChartPieSeriesOverlay)
Sets the pie segments effects overlay

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Pie(s => s.Sales, s => s.DateString).Overlay(ChartPieSeriesOverlay.None))
        .Render();
        %>

#### Parameters

##### overlay `Kendo.Mvc.UI.ChartPieSeriesOverlay`
The pie segment effects overlay.
            The default value is set in the theme.

### Connectors(System.Action\<Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder\>)
Configures the pie chart connectors.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(s => s.Sales, s => s.DateString)
        .Connectors(c => c
        .Color("red")
        );
        )
        %>

#### Parameters

##### configurator `System.Action<Kendo.Mvc.UI.Fluent.ChartPieConnectorsBuilder>`
The configuration action.