---
title:Kendo.Mvc.UI.Fluent.ChartAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaBuilder

## Methods

### Background(System.String)
Sets the chart area background color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Background("Red"))
        .Render();
        %>

#### Parameters

##### background `System.String`
The background color.