---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxislabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder

## Methods

### DateFormats(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisLabelsDateFormatsBuilder})
Culture to use for formatting the dates.
            See Globalization
            for more information.

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

##### culture `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisLabelsDateFormatsBuilder}`
Culture to use for formatting the dates.