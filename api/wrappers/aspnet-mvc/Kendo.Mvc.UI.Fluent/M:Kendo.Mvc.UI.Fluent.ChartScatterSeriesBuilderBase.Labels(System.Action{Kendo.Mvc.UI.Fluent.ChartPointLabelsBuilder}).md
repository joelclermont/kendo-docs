---
title:Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartscatterseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartScatterSeriesBuilderBase

## Methods

### Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder})
Configures the scatter chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Scatter(s => s.x, s => s.y)
        .Labels(labels => labels
        .Position(ChartBarLabelsPosition.Above)
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder}`
The configuration action.