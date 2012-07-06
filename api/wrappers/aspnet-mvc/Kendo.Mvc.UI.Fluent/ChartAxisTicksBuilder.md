---
title:Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisticksbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder

Defines the fluent interface for configuring .

## Methods

### Size(System.Int32)
Sets the ticks size

#### Example
    <% Html.Kendo().Chart()
        .Name("chart")
        .ValueAxis(axis => axis.MajorTicks(ticks => ticks.Size(2)))
        .Render();
        %>

#### Parameters

##### size `System.Int32`
The ticks size.

### Visible(System.Boolean)
Sets the ticks visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("chart")
        .ValueAxis(axis => axis.MajorTicks(ticks => ticks.Visible(false)))
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The ticks visibility.