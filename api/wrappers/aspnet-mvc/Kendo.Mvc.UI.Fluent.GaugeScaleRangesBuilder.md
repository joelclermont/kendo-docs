---
title:Kendo.Mvc.UI.Fluent.GaugeScaleRangesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugescalerangesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeScaleRangesBuilder

## Methods

### From(System.Double)
Sets the ranges start position.

#### Parameters

##### from `System.Double`
The ranges start position.

#### Parameters

##### from `System.Double`
The ranges start position.

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

### To(System.Double)
Sets the ranges end position.

#### Parameters

##### to `System.Double`
The ranges end position.

#### Parameters

##### to `System.Double`
The ranges end position.

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

### Color(System.String)
Sets the ranges color

#### Parameters

##### color `System.String`
The ranges color.

#### Parameters

##### color `System.String`
The ranges color.

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

### Opacity(System.Double)
Sets the ranges opacity

#### Parameters

##### opacity `System.Double`
The ranges opacity.

#### Parameters

##### opacity `System.Double`
The ranges opacity.

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