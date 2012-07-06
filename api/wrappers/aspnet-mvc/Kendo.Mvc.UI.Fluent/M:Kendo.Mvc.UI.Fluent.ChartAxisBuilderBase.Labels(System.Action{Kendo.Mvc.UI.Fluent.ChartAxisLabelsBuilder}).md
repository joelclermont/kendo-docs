---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder})
Configures the axis labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Labels(labels => labels
        .Color("Red")
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder}`
The configuration action.