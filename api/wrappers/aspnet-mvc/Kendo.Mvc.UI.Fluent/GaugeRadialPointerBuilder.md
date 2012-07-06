---
title:Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeradialpointerbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder

## Methods

### Cap(System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder})
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

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialCapBuilder}`
The configuration action.