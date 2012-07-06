---
title:Kendo.Mvc.UI.Fluent.LinearGaugeBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.lineargaugebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.LinearGaugeBuilder

Defines the fluent interface for configuring the  component.

## Methods

### Theme(System.String)
Sets the theme of the linear gauge.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Theme("Black")
        %>

#### Parameters

##### theme `System.String`
The linear gauge theme.

### GaugeArea(System.Action{Kendo.Mvc.UI.Fluent.GaugeAreaBuilder})
Sets the linear gauge area.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .ChartArea(chartArea => chartArea.margin(20))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeAreaBuilder}`
The linear gauge area.

### Scale(System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder})
Configures the scale

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .Min(10)
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder}`
The configurator

### Pointer(System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder})
Configures the pointer

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Pointer(pointer => pointer
        .Value(10)
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder}`
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