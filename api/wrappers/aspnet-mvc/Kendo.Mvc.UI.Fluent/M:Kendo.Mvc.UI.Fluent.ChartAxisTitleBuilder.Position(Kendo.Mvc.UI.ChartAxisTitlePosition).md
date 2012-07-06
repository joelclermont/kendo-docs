---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Position(Kendo.Mvc.UI.ChartAxisTitlePosition)
Sets the axis title position.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Position(ChartTitlePosition.Center)
        );
        )
        .Render();
        %>

#### Parameters

##### position `Kendo.Mvc.UI.ChartAxisTitlePosition`
The axis title position.