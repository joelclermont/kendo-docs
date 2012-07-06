---
title:Kendo.Mvc.UI.Fluent.ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

## Methods

### Text(System.String)
Sets the title text

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Text("Chart"))
        .Render();
        %>

#### Parameters

##### text `System.String`
The text title.