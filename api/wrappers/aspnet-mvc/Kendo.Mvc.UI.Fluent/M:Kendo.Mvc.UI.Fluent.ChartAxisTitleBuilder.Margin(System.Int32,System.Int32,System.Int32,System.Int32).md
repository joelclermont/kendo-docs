---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the axis title margin.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Margin(20, 20, 20, 20)
        );
        )
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The axis title top margin.

##### right `System.Int32`
The axis title right margin.

##### bottom `System.Int32`
The axis title bottom margin.

##### left `System.Int32`
The axis title left margin.