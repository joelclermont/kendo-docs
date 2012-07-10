---
title:ChartDateAxisLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxislabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder

Defines the fluent interface for configuring the chart labels.

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

### DateFormats(System.Action<Kendo.Mvc.UI.Fluent.ChartAxisLabelsDateFormatsBuilder>)
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

##### culture `System.Action<Kendo.Mvc.UI.Fluent.ChartAxisLabelsDateFormatsBuilder>`
Culture to use for formatting the dates.