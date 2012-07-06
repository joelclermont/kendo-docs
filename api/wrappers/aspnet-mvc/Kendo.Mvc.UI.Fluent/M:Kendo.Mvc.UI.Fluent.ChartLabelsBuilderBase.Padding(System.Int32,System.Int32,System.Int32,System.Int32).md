---
title:Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlabelsbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase

## Methods

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the labels padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Padding(0, 5, 5, 0)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The labels top padding.

##### right `System.Int32`
The labels right padding.

##### bottom `System.Int32`
The labels bottom padding.

##### left `System.Int32`
The labels left padding.