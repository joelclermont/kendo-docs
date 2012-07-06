---
title:Kendo.Mvc.UI.Fluent.ChartNegativeValueSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartnegativevaluesettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartNegativeValueSettingsBuilder

## Methods

### Visible(System.Boolean)
Sets the visibility for bubbles representing negative values

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bubble(s => s.x, s => s.y, s => s.size)
        .NegativeValues(n => n
        .Visible(true)
        );
        )
        .Render();
        %>

#### Parameters

##### visible `System.Boolean`
The visibility for bubbles representing negative values.