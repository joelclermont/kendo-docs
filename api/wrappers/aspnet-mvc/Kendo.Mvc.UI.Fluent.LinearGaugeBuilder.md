---
title:Kendo.Mvc.UI.Fluent.LinearGaugeBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.lineargaugebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.LinearGaugeBuilder

## Methods

### Theme(System.String)
Sets the theme of the linear gauge.

#### Parameters

##### theme `System.String`
The linear gauge theme.

#### Parameters

##### theme `System.String`
The linear gauge theme.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Theme("Black")
        %>

### GaugeArea(System.Action{Kendo.Mvc.UI.Fluent.GaugeAreaBuilder})
Sets the linear gauge area.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeAreaBuilder}`
The linear gauge area.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeAreaBuilder}`
The linear gauge area.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .ChartArea(chartArea => chartArea.margin(20))
        %>

### Scale(System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder})
Configures the scale

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder}`
The configurator

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder}`
The configurator

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .Min(10)
        )
        %>

### Pointer(System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder})
Configures the pointer

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder}`
The configurator

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder}`
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