---
title:Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeradialscalebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeRadialScaleBuilder

## Methods

### Labels(System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialScaleLabelsBuilder})
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

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeRadialScaleLabelsBuilder}`
The configuration action.