---
title:GaugeLinearScaleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelinearscalebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder

Defines the fluent interface for configuring the gauge scale.

## Properties

### linearGauge
The parent Guage

## Methods

### Mirror(System.Boolean)
Sets the mirror of the gauge

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("LinearGauge")
        .Scale(scale => scale
        .Mirror(true)
        )
        %>

#### Parameters

##### mirror `System.Boolean`
The mirror.

### Vertical(System.Boolean)
Sets the orientation of the gauge

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("LinearGauge")
        .Scale(scale => scale
        .Vertical(false)
        )
        %>

#### Parameters

##### vertical `System.Boolean`
The vertical.

### Labels(System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleLabelsBuilder})
Configures the labels.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Visible(false)
        )
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearScaleLabelsBuilder}`
The configuration action.