---
title:RadialGaugeBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.radialgaugebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.RadialGaugeBuilder

Defines the fluent interface for configuring the RadialGauge component.

## Methods

### Theme(System.String)
Sets the theme of the radial gauge.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Theme("Black")
        %>

#### Parameters

##### theme `System.String`
The radial gauge theme.

### GaugeArea(System.Action\<Kendo.Mvc.UI.Fluent.GaugeAreaBuilder\>)
Sets the radial gauge area.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .ChartArea(chartArea => chartArea.margin(20))
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.GaugeAreaBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/GaugeAreaBuilder)\>
The radial gauge area.

### Scale(System.Action\<Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder\>)
Configures the scale

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .Min(10)
        )
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/GaugeRadialScaleBuilder)\>
The configurator

### Pointer(System.Action\<Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder\>)
Configures the pointer

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Value(10)
        )
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.GaugeRadialPointerBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/GaugeRadialPointerBuilder)\>
The configurator

### Transitions(System.Boolean)
Enables or disabled animated transitions on initial load and refresh.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialScale")
        .Transitions(false)
        %>

#### Parameters

##### transitions `System.Boolean`
A value indicating if transition animations should be played.