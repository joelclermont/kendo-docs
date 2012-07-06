---
title:Kendo.Mvc.UI.Fluent.GaugeScaleRangesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugescalerangesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeScaleRangesBuilder

## Methods

### Opacity(System.Double)
Sets the ranges opacity

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Ranges(ranges => ranges
        .Add().Opacity(0.5);
        )
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`
The ranges opacity.