---
title:Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlabelsbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the labels border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Border(1, "Red", ChartDashType.Dot)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The labels border width.

##### color `System.String`
The labels border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The labels border dash type.