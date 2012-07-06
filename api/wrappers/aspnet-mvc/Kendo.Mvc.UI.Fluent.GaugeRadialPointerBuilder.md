---
title:Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeradialpointerbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder

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
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Color("red")
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
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Opacity(0.5)
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
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Value(25)
        )
        .Render();
        %>

### Cap(System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder})
Configures the pointer cap.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder}`
The configuration action.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Cap(cap => cap.Color("red"))
        )
        .Render();
        %>