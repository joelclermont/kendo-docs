---
title:Kendo.Mvc.UI.Fluent.ChartLegendBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlegendbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLegendBuilder

## Methods

### Visible(System.Boolean)
Sets the legend visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Visible(false))
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The legend visibility.