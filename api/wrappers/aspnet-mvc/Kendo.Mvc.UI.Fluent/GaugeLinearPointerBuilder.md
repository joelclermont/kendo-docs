---
title:Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelinearpointerbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLinearPointerBuilder

## Methods

### Track(System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearTrackBuilder})
Configures the pointer track.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Track(track => track.Visible(true))
        )
        .Render();
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeLinearTrackBuilder}`
The configuration action.