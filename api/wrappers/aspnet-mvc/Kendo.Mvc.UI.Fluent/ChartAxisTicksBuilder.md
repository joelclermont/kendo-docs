---
title:Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisticksbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder

## Methods

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