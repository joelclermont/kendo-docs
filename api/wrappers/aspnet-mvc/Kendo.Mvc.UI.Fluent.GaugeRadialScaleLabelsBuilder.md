---
title:Kendo.Mvc.UI.Fluent.GaugeRadialScaleLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeradialscalelabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeRadialScaleLabelsBuilder

## Methods

### Position(Kendo.Mvc.UI.GaugeRadialScaleLabelsPosition)
Sets the labels position

#### Parameters

##### position `Kendo.Mvc.UI.GaugeRadialScaleLabelsPosition`
The labels position.

#### Parameters

##### position `Kendo.Mvc.UI.GaugeRadialScaleLabelsPosition`
The labels position.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Position(GaugeRadialScaleLabelsPosition.Inside)
        )
        )
        %>