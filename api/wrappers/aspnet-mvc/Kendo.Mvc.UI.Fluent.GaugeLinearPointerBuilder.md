---
title:Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelinearpointerbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder

## Methods

### Color(System.String)
Sets the pointer color.

#### Parameters

##### color `System.String`
The pointer color.

#### Parameters

##### color `System.String`
The pointer color.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Color("red")
        )
        .Render();
        %>

### Shape(Kendo.Mvc.UI.GaugeLinearPointerShape)
Sets the pointer shape.

#### Parameters

##### shape `Kendo.Mvc.UI.GaugeLinearPointerShape`
The pointer shape.

#### Parameters

##### shape `Kendo.Mvc.UI.GaugeLinearPointerShape`
The pointer shape.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Shape(LinearGaugePointerShape.Arrow)
        )
        .Render();
        %>

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the pointer margin.

#### Parameters

##### top `System.Int32`
The pointer top margin.

##### right `System.Int32`
The pointer right margin.

##### bottom `System.Int32`
The pointer bottom margin.

##### left `System.Int32`
The pointer left margin.

#### Parameters

##### top `System.Int32`
The pointer top margin.

##### right `System.Int32`
The pointer right margin.

##### bottom `System.Int32`
The pointer bottom margin.

##### left `System.Int32`
The pointer left margin.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Margin(20, 20, 20, 20)
        )
        .Render();
        %>

### Margin(System.Int32)
Sets the pointer margin.

#### Parameters

##### margin `System.Int32`
The pointer margin.

#### Parameters

##### margin `System.Int32`
The pointer margin.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Margin(20)
        )
        .Render();
        %>

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the pointer border

#### Parameters

##### width `System.Int32`
The pointer border width.

##### color `System.String`
The pointer border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The pointer dash type.

#### Parameters

##### width `System.Int32`
The pointer border width.

##### color `System.String`
The pointer border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The pointer dash type.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Border(1, "#000", ChartDashType.Dot)
        )
        .Render();
        %>

### Opacity(System.Double)
Sets the pointer opacity.

#### Parameters

##### opacity `System.Double`

            The pointer opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

#### Parameters

##### opacity `System.Double`

            The pointer opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Opacity(0.5)
        )
        .Render();
        %>

### Size(System.Double)
Sets the pointer size.

#### Parameters

##### size `System.Double`
The pointer size.

#### Parameters

##### size `System.Double`
The pointer size.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Size(8)
        )
        .Render();
        %>

### Value(System.Double)
Sets the pointer value.

#### Parameters

##### value `System.Double`
The pointer value.

#### Parameters

##### value `System.Double`
The pointer value.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Value(25)
        )
        .Render();
        %>

### Track(System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearTrackBuilder})
Configures the pointer track.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearTrackBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearTrackBuilder}`
The configuration action.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Track(track => track.Visible(true))
        )
        .Render();
        %>