---
title:Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlabelsbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase

## Methods

### Font(System.String)
Sets the labels font

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Font("14px Arial,Helvetica,sans-serif")
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### font `System.String`
The labels font (CSS format).