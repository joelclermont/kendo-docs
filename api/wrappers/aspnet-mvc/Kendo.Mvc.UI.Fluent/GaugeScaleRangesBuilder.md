---
title:GaugeScaleRangesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugescalerangesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeScaleRangesBuilder

Defines the fluent interface for configuring ranges.

## Methods

### From(System.Double)
Sets the ranges start position.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Ranges(ranges => ranges
        .Add().From(1).Color("Red");
        )
        )
        .Render();
        %>

#### Parameters

##### from `System.Double`
The ranges start position.

### To(System.Double)
Sets the ranges end position.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Ranges(ranges => ranges
        .Add().To(2).Color("Red");
        )
        )
        .Render();
        %>

#### Parameters

##### to `System.Double`
The ranges end position.

### Color(System.String)
Sets the ranges color

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Ranges(ranges => ranges
        .Add().Color("Red");
        )
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The ranges color.

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