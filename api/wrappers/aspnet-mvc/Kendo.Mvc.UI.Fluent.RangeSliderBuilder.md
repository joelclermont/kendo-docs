---
title:Kendo.Mvc.UI.Fluent.RangeSliderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.rangesliderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.RangeSliderBuilder

## Methods

### 1.Values(System.Nullable{`0},System.Nullable{`0})
Sets the value of the range slider.

### 1.Values(`0[])
Sets the value of the range slider.

### 1.Orientation(Kendo.Mvc.UI.SliderOrientation)
Sets orientation of the range slider.

### 1.TickPlacement(Kendo.Mvc.UI.SliderTickPlacement)
Sets a value indicating how to display the tick marks on the range slider.

### 1.Min(`0)
Sets the minimum value of the range slider.

### 1.Max(`0)
Sets the maximum value of the range slider.

### 1.SmallStep(`0)
Sets the step with which the range slider value will change.

### 1.LargeStep(`0)
Sets the delta with which the value will change when user click on the track.

### 1.Tooltip(System.Boolean)
Display tooltip while drag.

### 1.Tooltip(System.Action{Kendo.Mvc.UI.Fluent.SliderTooltipBuilder})
Use it to configure tooltip while drag.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.SliderTooltipBuilder}`
Use builder to set different tooltip options.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.SliderTooltipBuilder}`
Use builder to set different tooltip options.

#### Example
    <%= Html.Kendo().Slider()
        .Name("Slider")
        .Tooltip(tooltip => tooltip
        .Enable(true)
        .Format("{0:P}")
        );
        %>

### 1.Events(System.Action{Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder})
Configures the client-side events.

#### Parameters

##### events `System.Action{Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder}`
The client events action.

#### Parameters

##### events `System.Action{Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder}`
The client events action.

#### Example
    <%= Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        .Events(events =>
        events.OnChange("onChange"))
        %>