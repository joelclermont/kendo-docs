---
title:Kendo.Mvc.UI.Fluent.ChartDateCategoryAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdatecategoryaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateCategoryAxisBuilder

## Methods

### Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder})
Configures the axis labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Date()
        .Labels(labels => labels
        .Culture(new CultureInfo("es-ES")
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder}`
The configuration action.