---
title:Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxislabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder

## Methods

### Skip(System.Int32)
Label rendering skip.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(product => product.Name)
        .Labels(labels => labels.Skip(2))
        )
        %>

#### Parameters

##### skip `System.Int32`
Skips rendering the first n labels.