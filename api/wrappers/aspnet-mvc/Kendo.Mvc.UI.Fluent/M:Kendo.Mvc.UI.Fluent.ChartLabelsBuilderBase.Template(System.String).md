---
title:Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlabelsbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase

## Methods

### Template(System.String)
Sets the labels template.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Template("${TotalSales}")
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### template `System.String`
The labels template.