---
title:Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpielabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder

## Methods

### Align(Kendo.Mvc.UI.ChartPieLabelsAlign)
Sets the labels align

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

#### Parameters

##### align `Kendo.Mvc.UI.ChartPieLabelsAlign`
The labels align.