---
title:Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesBuilderBase

## Methods

### Color(System.String)
Sets the bar fill color

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series.Bar(s => s.Sales).Color("Red"))
        .Render();
        %>

#### Parameters

##### color `System.String`
The bar fill color (CSS syntax).