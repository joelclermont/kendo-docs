---
title:Kendo.Mvc.UI.Fluent.ChartLegendBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartlegendbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartLegendBuilder

## Methods

### Font(System.String)
Sets the legend labels font

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Font("16px Arial,Helvetica,sans-serif"))
        .Render();
        %>

#### Parameters

##### font `System.String`
The legend labels font (CSS format).