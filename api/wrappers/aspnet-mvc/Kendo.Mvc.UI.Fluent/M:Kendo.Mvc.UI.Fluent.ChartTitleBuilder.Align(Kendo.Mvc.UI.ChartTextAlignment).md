---
title:Kendo.Mvc.UI.Fluent.ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

## Methods

### Align(Kendo.Mvc.UI.ChartTextAlignment)
Sets the title alignment

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Align(ChartTextAlignment.Left))
        .Render();
        %>

#### Parameters

##### align `Kendo.Mvc.UI.ChartTextAlignment`
The title alignment.