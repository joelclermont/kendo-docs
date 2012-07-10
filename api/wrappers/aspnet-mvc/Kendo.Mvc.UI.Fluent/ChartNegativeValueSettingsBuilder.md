---
title:ChartNegativeValueSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartnegativevaluesettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartNegativeValueSettingsBuilder

Defines the fluent interface for configuring ChartNegativeValueSettings.

## Methods

### Color(System.String)
Sets the color for bubbles representing negative values

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Series(series => series
        .Bubble(s => s.x, s => s.y, s => s.size)
        .NegativeValues(n => n
        .Visible(true)
        .Color("#ff0000")
        );
        )
        .Render();
        %>

#### Parameters

##### color `System.String`
The bubble color (CSS format).

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