---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder

## Methods

### MajorUnit(System.Double)
Sets the interval between major divisions in base units.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Date().BaseUnit(ChartAxisBaseUnit.Months).MajorUnit(4))
        %>

#### Parameters

##### majorUnit `System.Double`
The interval between major divisions in base units.