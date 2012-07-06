---
title:Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeradialcapbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder

## Methods

### Color(System.String)
Sets the cap color.

#### Parameters

##### color `System.String`
The cap color.

#### Parameters

##### color `System.String`
The cap color.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Cap(cap => cap.Color("red"))
        )
        .Render();
        %>

### Opacity(System.Double)
Sets the cap opacity.

#### Parameters

##### opacity `System.Double`

            The cap opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

#### Parameters

##### opacity `System.Double`

            The cap opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Cap(cap => cap.Opacity(0.5))
        )
        .Render();
        %>

### Size(System.Double)
Sets the cap size in percents.

#### Parameters

##### size `System.Double`
The cap size in percents.

#### Parameters

##### size `System.Double`
The cap size in percents.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Cap(cap => cap.Size(8))
        )
        .Render();
        %>