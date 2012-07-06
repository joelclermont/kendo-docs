---
title:Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelinearscalebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLinearScaleBuilder

## Methods

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