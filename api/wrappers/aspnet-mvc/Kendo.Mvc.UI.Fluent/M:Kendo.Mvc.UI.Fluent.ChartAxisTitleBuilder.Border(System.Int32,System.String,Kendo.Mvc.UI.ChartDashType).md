---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the axis title border

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Border(1, "#000", ChartDashType.Dot)
        );
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The axis title border width.

##### color `System.String`
The axis title border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The axis title dash type.