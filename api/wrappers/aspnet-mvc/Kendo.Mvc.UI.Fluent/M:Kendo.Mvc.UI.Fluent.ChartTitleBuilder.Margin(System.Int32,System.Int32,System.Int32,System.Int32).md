---
title:Kendo.Mvc.UI.Fluent.ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

## Methods

### Margin(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the title margin

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Margin(20))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The title top margin.

##### right `System.Int32`
The title right margin.

##### bottom `System.Int32`
The title bottom margin.

##### left `System.Int32`
The title left margin.