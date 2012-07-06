---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Background(System.String)
Sets the axis title background color.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Background("red")
        );
        )
        .Render();
        %>

#### Parameters

##### background `System.String`
The axis background color.