---
title:Kendo.Mvc.UI.Fluent.ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

## Methods

### Position(Kendo.Mvc.UI.ChartTitlePosition)
Sets the title position

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Position(ChartTitlePosition.Bottom))
        .Render();
        %>

#### Parameters

##### position `Kendo.Mvc.UI.ChartTitlePosition`
The title position.