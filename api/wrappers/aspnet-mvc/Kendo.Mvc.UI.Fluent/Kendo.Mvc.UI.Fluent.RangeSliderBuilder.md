---
title:Kendo.Mvc.UI.Fluent.RangeSliderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.rangesliderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.RangeSliderBuilder

## Methods

### Values(System.Nullable{`0},System.Nullable{`0})
Sets the value of the range slider.

### Values(`0[])
Sets the value of the range slider.

### Orientation(Kendo.Mvc.UI.SliderOrientation)
Sets orientation of the range slider.

### TickPlacement(Kendo.Mvc.UI.SliderTickPlacement)
Sets a value indicating how to display the tick marks on the range slider.

### Min(`0)
Sets the minimum value of the range slider.

### Max(`0)
Sets the maximum value of the range slider.

### SmallStep(`0)
Sets the step with which the range slider value will change.

### LargeStep(`0)
Sets the delta with which the value will change when user click on the track.

### Tooltip(System.Boolean)
Display tooltip while drag.

### Tooltip(System.Action{Kendo.Mvc.UI.Fluent.SliderTooltipBuilder})
Use it to configure tooltip while drag.

#### Example
    <%= Html.Kendo().Slider()
        .Name("Slider")
        .Tooltip(tooltip => tooltip
        .Enable(true)
        .Format("{0:P}")
        );
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.SliderTooltipBuilder}`
Use builder to set different tooltip options.

### Events(System.Action{Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder})
Configures the client-side events.

#### Example
    <%= Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        .Events(events =>
        events.OnChange("onChange"))
        %>

#### Parameters

##### events `System.Action{Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder}`
The client events action.