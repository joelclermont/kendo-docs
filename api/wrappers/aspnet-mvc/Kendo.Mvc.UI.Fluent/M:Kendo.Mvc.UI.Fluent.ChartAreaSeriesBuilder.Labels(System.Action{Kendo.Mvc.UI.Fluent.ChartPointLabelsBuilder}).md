---
title:Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartareaseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAreaSeriesBuilder

## Methods

### Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder})
Configures the area chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Area(s => s.Sales)
        .Labels(labels => labels
        .Position(ChartBarLabelsPosition.Above)
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartPointLabelsBuilder}`
The configuration action.