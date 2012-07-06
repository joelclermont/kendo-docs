---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxislabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder

## Methods

### Culture(System.Globalization.CultureInfo)
Culture to use for formatting the dates.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Date()
        .Categories(sale => sale.Date)
        .Labels(labels => labels.Culture(new CultureInfo("es-ES")))
        )
        %>

#### Parameters

##### culture `System.Globalization.CultureInfo`
Culture to use for formatting the dates.