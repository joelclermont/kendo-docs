---
title:ChartBarSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbarseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBarSeriesBuilder

Defines the fluent interface for configuring bar series.

## Methods

### Stack(System.Boolean)
Sets a value indicating if the bars should be stacked.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Stack(true))
        %>

#### Parameters

##### stacked `System.Boolean`
A value indicating if the bars should be stacked.

### Stack(System.String)
Sets the name of the stack that this series belongs to. Each unique name creates a new stack.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Stack("Female"))
        %>

#### Parameters

##### stacked `System.String`
The name of the stack.

### Aggregate(Kendo.Mvc.UI.ChartSeriesAggregate)
Sets the aggregate function for date series.
            This function is used when a category (an year, month, etc.) contains two or more points.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Aggregate())
        %>

#### Parameters

##### aggregate `Kendo.Mvc.UI.ChartSeriesAggregate`
Aggregate function name.

### Gap(System.Double)
Set distance between category clusters.
            
            A value of 1 means that there is a total of 1 column width / bar height between categories.
            The distance is distributed evenly on each side.
            The default value is 1.5

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Gap(1))
        %>

### Spacing(System.Double)
Sets a value indicating the distance between bars / categories.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Spacing(s => s.Sales).Spacing(1))
        %>

#### Parameters

##### spacing `System.Double`
Value of 1 means that the distance between bars is equal to their width.
            The default value is 0

### Labels(System.Action\<Kendo.Mvc.UI.Fluent.ChartBarLabelsBuilder\>)
Configures the bar chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Position(ChartBarLabelsPosition.InsideEnd)
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action<Kendo.Mvc.UI.Fluent.ChartBarLabelsBuilder>`
The configuration action.

### Labels(System.Boolean)
Sets the visibility of bar chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(true);
        )
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the bars border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Border("1", "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The bars border width.

##### color `System.String`
The bars border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The bars border dash type.

### Overlay(Kendo.Mvc.UI.ChartBarSeriesOverlay)
Sets the bar effects overlay

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Overlay(ChartBarSeriesOverlay.None))
        .Render();
        %>

#### Parameters

##### overlay `Kendo.Mvc.UI.ChartBarSeriesOverlay`
The bar effects overlay. The default is ChartBarSeriesOverlay.Glass