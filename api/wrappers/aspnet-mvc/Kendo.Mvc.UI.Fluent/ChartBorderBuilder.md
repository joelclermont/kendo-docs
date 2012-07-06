---
title:Kendo.Mvc.UI.Fluent.ChartBorderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartborderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBorderBuilder

## Methods

### DashType(Kendo.Mvc.UI.ChartDashType)
Sets the border dashType.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.Border(border => border.DashType(ChartDashType.Dot)))
        .Render();
        %>

#### Parameters

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dashType.