---
title:Kendo.Mvc.UI.Fluent.SliderTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.slidertooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SliderTooltipBuilder

## Methods

### Format(System.String)
Gets or sets the format for displaying the value in the tooltip.

#### Example
    <%= Html.Kendo().Slider()
        .Name("Slider")
        .Tooltip(tooltip => tooltip.Format("{0:P"))
        %>

#### Parameters

##### value `System.String`
The value.

### Enabled(System.Boolean)
Display tooltip while drag.

#### Example
    <%= Html.Kendo().Slider()
        .Name("Slider")
        .Tooltip(tooltip => tooltip.Enable(false))
        %>

#### Parameters

##### value `System.Boolean`
The value.