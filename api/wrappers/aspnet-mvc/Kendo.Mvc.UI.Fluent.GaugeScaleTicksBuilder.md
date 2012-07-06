---
title:Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugescaleticksbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder

## Methods

### Color(System.String)
Sets the ticks color

#### Parameters

##### color `System.String`
The ticks color (CSS format).

#### Parameters

##### color `System.String`
The ticks color (CSS format).

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.Color("#f00")))
        .Render();
        %>

### Width(System.Int32)
Sets the ticks width

#### Parameters

##### width `System.Int32`
The ticks width.

#### Parameters

##### width `System.Int32`
The ticks width.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.Width(2)))
        .Render();
        %>

### Size(System.Int32)
Sets the ticks size

#### Parameters

##### size `System.Int32`
The ticks size.

#### Parameters

##### size `System.Int32`
The ticks size.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.Size(2)))
        .Render();
        %>

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the ticks dashType

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The ticks dashType.

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The ticks dashType.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.DashType(ChartDashType.Dot)))
        .Render();
        %>

### Visible(System.Boolean)
Sets the ticks visibility

#### Parameters

##### visible `System.Boolean`
The ticks visibility.

#### Parameters

##### visible `System.Boolean`
The ticks visibility.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.Visible(false)))
        .Render();
        %>