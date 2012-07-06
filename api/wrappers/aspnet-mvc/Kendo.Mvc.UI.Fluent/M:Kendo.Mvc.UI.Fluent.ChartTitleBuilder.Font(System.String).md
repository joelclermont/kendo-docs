---
title:Kendo.Mvc.UI.Fluent.ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

## Methods

### Font(System.String)
Sets the title font

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Font("16px Arial,Helvetica,sans-serif"))
        .Render();
        %>

#### Parameters

##### font `System.String`
The title font (CSS format).