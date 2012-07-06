---
title:Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlabelsbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLabelsBuilderBase

## Methods

### Opacity(System.Double)
Sets the labels opacity.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bar(s => s.Sales)
        .Labels(labels => labels
        .Opacity(0.5)
        .Visible(true);
        );
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            