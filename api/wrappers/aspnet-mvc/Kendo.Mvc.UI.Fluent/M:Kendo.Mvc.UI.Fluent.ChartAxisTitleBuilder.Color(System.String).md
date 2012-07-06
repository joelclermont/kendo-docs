---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Color(System.String)
Sets the axis title text color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Color("red")
        );
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The axis text color.