---
title:Kendo.Mvc.UI.Fluent.RadialGaugeBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.radialgaugebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.RadialGaugeBuilder

## Methods

### Theme(System.String)
Sets the theme of the radial gauge.

#### Parameters

##### theme `System.String`
The radial gauge theme.

#### Parameters

##### theme `System.String`
The radial gauge theme.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Theme("Black")
        %>

### GaugeArea(System.Action{Kendo.Mvc.UI.Fluent.GaugeAreaBuilder})
Sets the radial gauge area.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeAreaBuilder}`
The radial gauge area.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeAreaBuilder}`
The radial gauge area.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .ChartArea(chartArea => chartArea.margin(20))
        %>

### Scale(System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder})
Configures the scale

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder}`
The configurator

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder}`
The configurator

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .Min(10)
        )
        %>

### Pointer(System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder})
Configures the pointer

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder}`
The configurator

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder}`
The configurator

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Value(10)
        )
        %>

### Transitions(System.Boolean)
Enables or disabled animated transitions on initial load and refresh.

#### Parameters

##### transitions `System.Boolean`

            A value indicating if transition animations should be played.
            

#### Parameters

##### transitions `System.Boolean`

            A value indicating if transition animations should be played.
            

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialScale")
        .Transitions(false)
        %>