---
title:Kendo.Mvc.UI.Fluent.SliderTooltipBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.slidertooltipbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SliderTooltipBuilder

## Methods

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