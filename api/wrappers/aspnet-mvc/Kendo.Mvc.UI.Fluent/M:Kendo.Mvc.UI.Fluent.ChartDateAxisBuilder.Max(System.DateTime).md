---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder

## Methods

### Max(System.DateTime)
Sets the end date of the axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Date().Max(DateTime.Parse("2012/01/01")))
        %>

#### Parameters

##### max `System.DateTime`
The end date of the axis.