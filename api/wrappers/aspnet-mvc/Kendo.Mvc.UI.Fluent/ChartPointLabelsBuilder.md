---
title:Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpointlabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder

Defines the fluent interface for configuring the chart data labels.

## Methods

### Position(Kendo.Mvc.UI.ChartPointLabelsPosition)
Sets the labels position

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Line(s => s.Sales)
        .Labels(labels => labels
        .Position(ChartPointLabelsPosition.Above)
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### position `Kendo.Mvc.UI.ChartPointLabelsPosition`
The labels position.