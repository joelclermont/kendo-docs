---
title:Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelinearscalebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder

## Methods

### Mirror(System.Boolean)
Sets the mirror of the gauge

#### Parameters

##### mirror `System.Boolean`
The mirror.

#### Parameters

##### mirror `System.Boolean`
The mirror.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("LinearGauge")
        .Scale(scale => scale
        .Mirror(true)
        )
        %>

### Vertical(System.Boolean)
Sets the orientation of the gauge

#### Parameters

##### vertical `System.Boolean`
The vertical.

#### Parameters

##### vertical `System.Boolean`
The vertical.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("LinearGauge")
        .Scale(scale => scale
        .Vertical(false)
        )
        %>

### Labels(System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleLabelsBuilder})
Configures the labels.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleLabelsBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleLabelsBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Visible(false)
        )
        )
        %>