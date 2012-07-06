---
title:Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlabelsbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase

## Methods

### Rotation(System.Int32)
Sets the labels text rotation

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Rotation(45)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### rotation `System.Int32`
The labels text rotation.