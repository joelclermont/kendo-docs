---
title:Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlabelsbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase

## Methods

### Format(System.String)
Sets the labels format.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Format("{0:C}")
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### format `System.String`
The labels format.