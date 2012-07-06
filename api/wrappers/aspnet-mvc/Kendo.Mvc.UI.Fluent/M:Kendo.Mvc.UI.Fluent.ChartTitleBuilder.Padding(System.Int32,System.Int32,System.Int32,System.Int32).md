---
title:Kendo.Mvc.UI.Fluent.ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

## Methods

### Padding(System.Int32,System.Int32,System.Int32,System.Int32)
Sets the title padding

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Padding(20))
        .Render();
        %>

#### Parameters

##### top `System.Int32`
The title top padding.

##### right `System.Int32`
The title right padding.

##### bottom `System.Int32`
The title bottom padding.

##### left `System.Int32`
The title left padding.