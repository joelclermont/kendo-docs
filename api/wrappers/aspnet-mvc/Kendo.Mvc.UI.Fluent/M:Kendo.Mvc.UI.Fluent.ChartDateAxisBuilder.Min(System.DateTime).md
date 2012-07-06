---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder

## Methods

### Min(System.DateTime)
Sets the start date of the axis.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Date().Min(DateTime.Parse("2012/01/01")))
        %>

#### Parameters

##### min `System.DateTime`
The start date of the axis.