---
title:ChartMarkersBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartmarkersbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartMarkersBuilder

Defines the fluent interface for configuring the chart data labels.

## Methods

### Type(Kendo.Mvc.UI.ChartMarkerShape)
Sets the markers shape type.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Type(ChartMarkerShape.Triangle)
        );
        )
        .Render();
        %>

#### Parameters

##### type [Kendo.Mvc.UI.ChartMarkerShape](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/ChartMarkerShape)
The markers shape type.

### Size(System.Int32)
Sets the markers size.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Size(10)
        );
        )
        .Render();
        %>

#### Parameters

##### size `System.Int32`
The markers size.

### Visible(System.Boolean)
Sets the markers visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The markers visibility.

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the markers border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Border(1, "Red", ChartDashType.Dot)
        );
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The markers border width.

##### color `System.String`
The markers border color (CSS syntax).

##### dashType [Kendo.Mvc.UI.ChartDashType](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/ChartDashType)
The markers border dash type.

### Background(System.String)
The background color of the current series markers.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Markers(markers => markers
        .Background("Red");
        );
        )
        .Render();
        %>

#### Parameters

##### backgorund `System.String`
The background color of the current series markers. The background color is series color.