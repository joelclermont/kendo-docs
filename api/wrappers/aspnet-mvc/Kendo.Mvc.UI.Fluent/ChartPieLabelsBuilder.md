---
title:Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpielabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder

## Methods

### Position(Kendo.Mvc.UI.ChartPieLabelsPosition)
Sets the labels position

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(p => p.Sales)
        .Labels(labels => labels
        .Position(ChartPieLabelsPosition.Center)
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### position `Kendo.Mvc.UI.ChartPieLabelsPosition`
The labels position.