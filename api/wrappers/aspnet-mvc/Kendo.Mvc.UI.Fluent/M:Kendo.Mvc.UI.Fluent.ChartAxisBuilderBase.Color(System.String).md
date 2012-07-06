---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### Color(System.String)
Sets the color for all axis elements. Can be overriden by individual settings.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Color("#ff0000")
        )
        %>

#### Parameters

##### color `System.String`
The axis color.