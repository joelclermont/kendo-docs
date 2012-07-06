---
title:Kendo.Mvc.UI.Fluent.ChartMarkersBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartmarkersbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartMarkersBuilder

## Methods

### Type(Kendo.Mvc.UI.ChartMarkerShape)
Sets the markers shape type.

#### Parameters

##### type `Kendo.Mvc.UI.ChartMarkerShape`
The markers shape type.

#### Parameters

##### type `Kendo.Mvc.UI.ChartMarkerShape`
The markers shape type.

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

### Size(System.Int32)
Sets the markers size.

#### Parameters

##### size `System.Int32`
The markers size.

#### Parameters

##### size `System.Int32`
The markers size.

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

### Visible(System.Boolean)
Sets the markers visibility

#### Parameters

##### visible `System.Boolean`
The markers visibility.

#### Parameters

##### visible `System.Boolean`
The markers visibility.

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

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the markers border

#### Parameters

##### width `System.Int32`
The markers border width.

##### color `System.String`
The markers border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The markers border dash type.

#### Parameters

##### width `System.Int32`
The markers border width.

##### color `System.String`
The markers border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The markers border dash type.

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

### Background(System.String)
The background color of the current series markers.

#### Parameters

##### backgorund `System.String`
The background color of the current series markers. The background color is series color.

#### Parameters

##### backgorund `System.String`
The background color of the current series markers. The background color is series color.

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