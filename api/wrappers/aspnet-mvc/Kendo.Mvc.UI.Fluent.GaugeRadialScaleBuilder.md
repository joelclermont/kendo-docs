---
title:Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeradialscalebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder

## Methods

### EndAngle(System.Double)
Sets the end angle of the gauge

#### Parameters

##### endAngle `System.Double`
The end angle.

#### Parameters

##### endAngle `System.Double`
The end angle.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .EndAngle(10)
        )
        %>

### StartAngle(System.Double)
Sets the start angle of the gauge

#### Parameters

##### startAngle `System.Double`
The start Angle.

#### Parameters

##### startAngle `System.Double`
The start Angle.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .StartAngle(220)
        )
        %>

### Labels(System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialScaleLabelsBuilder})
Configures the labels.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialScaleLabelsBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialScaleLabelsBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Visible(false)
        )
        )
        %>