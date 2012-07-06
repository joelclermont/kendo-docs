---
title:Kendo.Mvc.UI.Fluent.ChartBarLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbarlabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBarLabelsBuilder

## Methods

### Position(Kendo.Mvc.UI.ChartBarLabelsPosition)
Sets the labels position

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Position(ChartBarLabelsPosition.InsideEnd)
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### position `Kendo.Mvc.UI.ChartBarLabelsPosition`
The labels position.