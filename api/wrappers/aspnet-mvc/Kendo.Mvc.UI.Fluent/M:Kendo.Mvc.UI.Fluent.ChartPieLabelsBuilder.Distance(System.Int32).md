---
title:Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpielabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder

## Methods

### Distance(System.Int32)
Sets the labels distance

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(p => p.Sales)
        .Labels(labels => labels
        .Distance(20)
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### distance `System.Int32`
The labels distance.