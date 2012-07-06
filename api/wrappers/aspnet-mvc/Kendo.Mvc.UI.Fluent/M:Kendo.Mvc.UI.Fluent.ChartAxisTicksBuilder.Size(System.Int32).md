---
title:Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisticksbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder

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