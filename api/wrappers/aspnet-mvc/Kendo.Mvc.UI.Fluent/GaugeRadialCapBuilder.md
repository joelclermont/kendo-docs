---
title:Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeradialcapbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder

Defines the fluent interface for configuring the RadialGaugeCap.

## Methods

### Color(System.String)
Sets the cap color.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Cap(cap => cap.Color("red"))
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The cap color.

### Opacity(System.Double)
Sets the cap opacity.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Cap(cap => cap.Opacity(0.5))
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`
The cap opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.

### Size(System.Double)
Sets the cap size in percents.

#### Example
    <% Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Cap(cap => cap.Size(8))
        )
        .Render();
        %>

#### Parameters

##### size `System.Double`
The cap size in percents.