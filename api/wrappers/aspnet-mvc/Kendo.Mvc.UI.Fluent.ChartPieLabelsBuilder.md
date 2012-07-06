---
title:Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpielabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder

## Methods

### Align(Kendo.Mvc.UI.ChartPieLabelsAlign)
Sets the labels align

#### Parameters

##### align `Kendo.Mvc.UI.ChartPieLabelsAlign`
The labels align.

#### Parameters

##### align `Kendo.Mvc.UI.ChartPieLabelsAlign`
The labels align.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(p => p.Sales)
        .Labels(labels => labels
        .Align(ChartPieLabelsAlign.Column)
        .Visible(true)
        );
        )
        .Render();
        %>

### Distance(System.Int32)
Sets the labels distance

#### Parameters

##### distance `System.Int32`
The labels distance.

#### Parameters

##### distance `System.Int32`
The labels distance.

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

### Position(Kendo.Mvc.UI.ChartPieLabelsPosition)
Sets the labels position

#### Parameters

##### position `Kendo.Mvc.UI.ChartPieLabelsPosition`
The labels position.

#### Parameters

##### position `Kendo.Mvc.UI.ChartPieLabelsPosition`
The labels position.

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