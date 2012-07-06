---
title:Kendo.Mvc.UI.Fluent.GaugeScaleBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugescalebuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeScaleBuilderBase

## Methods

### 2.MinorTicks(System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder})
Configures the minor ticks.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .MinorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder}`
The configuration action.

### 2.MajorTicks(System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder})
Configures the major ticks.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .MajorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder}`
The configuration action.

### 2.Ranges(System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleRangesFactory{`0}})
Defines the ranges items.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Ranges.Add()
        .From(1)
        .To(2)
        )
        %>

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleRangesFactory{`0}}`
The add action.

### 2.MajorUnit(System.Double)
Sets the scale major unit.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.MajorUnit(5))
        %>

#### Parameters

##### majorUnit `System.Double`
The major unit.

### 2.MinorUnit(System.Double)
Sets the scale minor unit.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.MinorUnit(5))
        %>

#### Parameters

##### minorUnit `System.Double`
The minor unit.

### 2.Min(System.Double)
Sets the scale min value.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.Min(-20))
        %>

#### Parameters

##### min `System.Double`
The min.

### 2.Max(System.Double)
Sets the scale max value.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.Max(20))
        %>

#### Parameters

##### max `System.Double`
The max.

### 2.Reverse(System.Boolean)
Sets the scale reverse.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.reverse(true))
        %>

#### Parameters

##### reverse `System.Boolean`
The scale reverse.