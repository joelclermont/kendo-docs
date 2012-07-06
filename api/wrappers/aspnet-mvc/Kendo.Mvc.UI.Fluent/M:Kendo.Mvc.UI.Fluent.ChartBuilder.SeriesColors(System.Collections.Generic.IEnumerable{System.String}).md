---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### SeriesColors(System.Collections.Generic.IEnumerable{System.String})
Sets the series colors.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .SeriesColors(new string[] { "#f00", "#0f0", "#00f" })
        %>

#### Parameters

##### colors `System.Collections.Generic.IEnumerable{System.String}`
A list of the series colors.