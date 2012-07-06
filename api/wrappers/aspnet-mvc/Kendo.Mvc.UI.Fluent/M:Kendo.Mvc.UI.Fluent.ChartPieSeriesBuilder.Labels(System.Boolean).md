---
title:Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartpieseriesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartPieSeriesBuilder

## Methods

### Labels(System.Boolean)
Sets the visibility of pie chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Pie(s => s.Sales, s => s.DateString)
        .Labels(true);
        )
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.