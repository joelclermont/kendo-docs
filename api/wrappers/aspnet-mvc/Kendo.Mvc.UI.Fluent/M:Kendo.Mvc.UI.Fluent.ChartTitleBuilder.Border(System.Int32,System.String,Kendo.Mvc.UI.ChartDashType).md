---
title:Kendo.Mvc.UI.Fluent.ChartTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charttitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartTitleBuilder

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the title border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The title border width.

##### color `System.String`
The title border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The title dash type.