---
title:Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlineseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLineSeriesBuilder

## Methods

### Aggregate(Kendo.Mvc.UI.ChartSeriesAggregate)
Sets the aggregate function for date series.
            This function is used when a category (an year, month, etc.) contains two or more points.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series => series.Line(s => s.Sales).Aggregate())
        %>

#### Parameters

##### aggregate `Kendo.Mvc.UI.ChartSeriesAggregate`
Aggregate function name.