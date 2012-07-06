---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Text(System.String)
Sets the axis title text.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Text("Axis")
        );
        )
        .Render();
        %>

#### Parameters

##### text `System.String`
The text of the axis title.