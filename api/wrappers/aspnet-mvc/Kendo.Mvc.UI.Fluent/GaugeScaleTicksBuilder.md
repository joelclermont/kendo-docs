---
title:GaugeScaleTicksBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugescaleticksbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder

Defines the fluent interface for configuring GaugeScaleTicks.

## Methods

### Color(System.String)
Sets the ticks color

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.Color("#f00")))
        .Render();
        %>

#### Parameters

##### color `System.String`
The ticks color (CSS format).

### Width(System.Int32)
Sets the ticks width

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.Width(2)))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The ticks width.

### Size(System.Int32)
Sets the ticks size

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.Size(2)))
        .Render();
        %>

#### Parameters

##### size `System.Int32`
The ticks size.

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the ticks dashType

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale.MajorTicks(ticks => ticks.DashType(ChartDashType.Dot)))
        .Render();
        %>

#### Parameters

##### dashType [Kendo.Mvc.UI.ChartDashType](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/ChartDashType)
The ticks dashType.

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