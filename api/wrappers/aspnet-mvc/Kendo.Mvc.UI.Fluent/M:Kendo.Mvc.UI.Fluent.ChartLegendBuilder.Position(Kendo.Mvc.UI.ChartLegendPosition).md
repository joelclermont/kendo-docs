---
title:Kendo.Mvc.UI.Fluent.ChartLegendBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlegendbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLegendBuilder

## Methods

### Position(Kendo.Mvc.UI.ChartLegendPosition)
Sets the legend position

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Position(ChartLegendPosition.Bottom))
        .Render();
        %>

#### Parameters

##### position `Kendo.Mvc.UI.ChartLegendPosition`
The legend position.