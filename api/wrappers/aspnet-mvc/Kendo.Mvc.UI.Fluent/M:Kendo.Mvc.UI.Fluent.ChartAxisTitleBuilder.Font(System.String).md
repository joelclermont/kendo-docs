---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Font(System.String)
Sets the axis title font.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Font("16px Arial,Helvetica,sans-serif")
        );
        )
        .Render();
        %>

#### Parameters

##### font `System.String`
The axis title font (CSS format).