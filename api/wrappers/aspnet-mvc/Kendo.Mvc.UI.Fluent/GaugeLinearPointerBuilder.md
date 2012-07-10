---
title:GaugeLinearPointerBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelinearpointerbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder

Defines the fluent interface for configuring the GaugeLinearPointer.

## Methods

### Color(System.String)
Sets the pointer color.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Color("red")
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The pointer color.

### Shape(Kendo.Mvc.UI.GaugeLinearPointerShape)
Sets the pointer shape.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Shape(LinearGaugePointerShape.Arrow)
        )
        .Render();
        %>

#### Parameters

##### shape [Kendo.Mvc.UI.GaugeLinearPointerShape](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/GaugeLinearPointerShape)
The pointer shape.

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the pointer margin.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Margin(20, 20, 20, 20)
        )
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The pointer top margin.

##### right `System.Int32`
The pointer right margin.

##### bottom `System.Int32`
The pointer bottom margin.

##### left `System.Int32`
The pointer left margin.

### Margin(System.Int32)
Sets the pointer margin.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Margin(20)
        )
        .Render();
        %>

#### Parameters

##### margin `System.Int32`
The pointer margin.

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the pointer border

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Border(1, "#000", ChartDashType.Dot)
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The pointer border width.

##### color `System.String`
The pointer border color.

##### dashType [Kendo.Mvc.UI.ChartDashType](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/ChartDashType)
The pointer dash type.

### Opacity(System.Double)
Sets the pointer opacity.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Opacity(0.5)
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`
The pointer opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.

### Size(System.Double)
Sets the pointer size.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Size(8)
        )
        .Render();
        %>

#### Parameters

##### size `System.Double`
The pointer size.

### Value(System.Double)
Sets the pointer value.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Value(25)
        )
        .Render();
        %>

#### Parameters

##### value `System.Double`
The pointer value.

### Track(System.Action\<Kendo.Mvc.UI.Fluent.GaugeLinearTrackBuilder\>)
Configures the pointer track.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Track(track => track.Visible(true))
        )
        .Render();
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.GaugeLinearTrackBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/GaugeLinearTrackBuilder)\>
The configuration action.