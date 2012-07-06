---
title:Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugescaleticksbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder

## Methods

### Visible(System.Boolean)
Sets the ticks visibility

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.Visible(false)))
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The ticks visibility.