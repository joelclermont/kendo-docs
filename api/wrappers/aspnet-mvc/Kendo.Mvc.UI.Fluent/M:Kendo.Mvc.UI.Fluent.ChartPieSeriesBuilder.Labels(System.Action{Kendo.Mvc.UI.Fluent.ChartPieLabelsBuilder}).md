---
title:Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder

## Methods

### Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder})
Configures the pie chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(s => s.Sales, s => s.DateString)
        .Labels(labels => labels
        .Color("red")
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartPieLabelsBuilder}`
The configuration action.