---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder

## Methods

### MinorUnit(System.Double)
Sets the interval between minor divisions in base units.
            It defaults to 1/5th of the majorUnit

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Date().BaseUnit(ChartAxisBaseUnit.Days).MajorUnit(4).MinorUnit(2))
        %>

#### Parameters

##### majorUnit `System.Double`
The interval between minor divisions in base units.