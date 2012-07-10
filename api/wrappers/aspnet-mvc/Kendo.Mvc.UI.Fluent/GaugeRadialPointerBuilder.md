---
title:GaugeRadialPointerBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeradialpointerbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder

Defines the fluent interface for configuring the !:GaugeRadialPointer{T}.

## Methods

### Color(System.String)
Sets the pointer color.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Color("red")
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The pointer color.

### Opacity(System.Double)
Sets the pointer opacity.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Opacity(0.5)
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`
The pointer opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.

### Value(System.Double)
Sets the pointer value.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Value(25)
        )
        .Render();
        %>

#### Parameters

##### value `System.Double`
The pointer value.

### Cap(System.Action\<Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder\>)
Configures the pointer cap.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Cap(cap => cap.Color("red"))
        )
        .Render();
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/GaugeRadialCapBuilder)\>
The configuration action.