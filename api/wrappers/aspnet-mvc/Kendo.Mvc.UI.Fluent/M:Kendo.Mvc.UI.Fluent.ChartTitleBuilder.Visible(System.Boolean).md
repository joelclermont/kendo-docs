---
title:Kendo.Mvc.UI.Fluent.ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

## Methods

### Visible(System.Boolean)
Sets the title visibility

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Visible(false))
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The title visibility.