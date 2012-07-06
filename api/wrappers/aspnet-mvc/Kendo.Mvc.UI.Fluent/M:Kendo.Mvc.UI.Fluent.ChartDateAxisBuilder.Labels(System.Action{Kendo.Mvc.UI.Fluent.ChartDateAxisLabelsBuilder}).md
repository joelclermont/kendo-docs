---
title:Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartdateaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartDateAxisBuilder

## Methods

### Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartDateAxisLabelsBuilder})
Configures the axis labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .XAxis(axis => axis
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