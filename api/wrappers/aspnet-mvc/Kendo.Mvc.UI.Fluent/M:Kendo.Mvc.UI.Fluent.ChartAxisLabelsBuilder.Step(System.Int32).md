---
title:Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxislabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder

## Methods

### Step(System.Int32)
Label rendering step.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(product => product.Name)
        .Labels(labels => labels.Step(2))
        )
        %>

#### Parameters

##### step `System.Int32`
A value indicating the step at which labels are rendered.
            Every n-th label is rendered where n is the step.