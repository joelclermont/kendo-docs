---
title:Kendo.Mvc.UI.Fluent.GaugeScaleBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugescalebuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeScaleBuilderBase

## Methods

### 2.MinorTicks(System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder})
Configures the minor ticks.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .MinorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

### 2.MajorTicks(System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder})
Configures the major ticks.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleTicksBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .MajorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

### 2.Ranges(System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleRangesFactory{`0}})
Defines the ranges items.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleRangesFactory{`0}}`
The add action.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.GaugeScaleRangesFactory{`0}}`
The add action.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Ranges.Add()
        .From(1)
        .To(2)
        )
        %>

### 2.MajorUnit(System.Double)
Sets the scale major unit.

#### Parameters

##### majorUnit `System.Double`
The major unit.

#### Parameters

##### majorUnit `System.Double`
The major unit.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.MajorUnit(5))
        %>

### 2.MinorUnit(System.Double)
Sets the scale minor unit.

#### Parameters

##### minorUnit `System.Double`
The minor unit.

#### Parameters

##### minorUnit `System.Double`
The minor unit.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.MinorUnit(5))
        %>

### 2.Min(System.Double)
Sets the scale min value.

#### Parameters

##### min `System.Double`
The min.

#### Parameters

##### min `System.Double`
The min.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.Min(-20))
        %>

### 2.Max(System.Double)
Sets the scale max value.

#### Parameters

##### max `System.Double`
The max.

#### Parameters

##### max `System.Double`
The max.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.Max(20))
        %>

### 2.Reverse(System.Boolean)
Sets the scale reverse.

#### Parameters

##### reverse `System.Boolean`
The scale reverse.

#### Parameters

##### reverse `System.Boolean`
The scale reverse.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => sclae.reverse(true))
        %>