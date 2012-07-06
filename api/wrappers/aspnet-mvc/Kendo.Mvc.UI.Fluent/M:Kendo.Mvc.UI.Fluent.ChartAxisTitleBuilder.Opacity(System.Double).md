---
title:Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxistitlebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder

## Methods

### Opacity(System.Double)
Sets the axis title opacity.

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Title(title => title
        .Opacity(0.5)
        );
        )
        .Render();
        %>

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            