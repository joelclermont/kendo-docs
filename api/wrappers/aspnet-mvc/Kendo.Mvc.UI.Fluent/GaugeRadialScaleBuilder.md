---
title:GaugeRadialScaleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeradialscalebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder

Defines the fluent interface for configuring the gauge scale.

## Properties

### radialGauge
The parent Guage

## Methods

### EndAngle(System.Double)
Sets the end angle of the gauge

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .EndAngle(10)
        )
        %>

#### Parameters

##### endAngle `System.Double`
The end angle.

### StartAngle(System.Double)
Sets the start angle of the gauge

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .StartAngle(220)
        )
        %>

#### Parameters

##### startAngle `System.Double`
The start Angle.

### Labels(System.Action<Kendo.Mvc.UI.Fluent.GaugeRadialScaleLabelsBuilder>)
Configures the labels.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Visible(false)
        )
        )
        %>

#### Parameters

##### configurator System.Action<[Kendo.Mvc.UI.Fluent.GaugeRadialScaleLabelsBuilder>](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/GaugeRadialScaleLabelsBuilder>)>
The configuration action.