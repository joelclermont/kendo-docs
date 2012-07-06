---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### DataSource(System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyAjaxDataSourceBuilder{`0}})
Data Source configuration

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .DataSource(ds =>
        {
        ds.Ajax().Read(r => r.Action("SalesData", "Chart"));
        })
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyAjaxDataSourceBuilder{`0}}`
Use the configurator to set different data binding options.