---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the axis title padding.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Padding(20, 20, 20, 20)
        );
        )
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The axis title top padding.

##### right `System.Int32`
The axis title right padding.

##### bottom `System.Int32`
The axis title bottom padding.

##### left `System.Int32`
The axis title left padding.