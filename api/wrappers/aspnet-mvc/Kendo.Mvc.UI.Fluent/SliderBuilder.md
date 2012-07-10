---
title:SliderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.sliderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SliderBuilder

Defines the fluent interface for configuring the !:Slider{T}component.

## Methods

### Value(System.Nullable{})
Sets the value of the slider.

### IncreaseButtonTitle(System.String)
Sets the title of the slider increase button.

### ShowButtons(System.Nullable{System.Boolean})
Sets whether slider to be rendered with increase/decrease button.

### DecreaseButtonTitle(System.String)
Sets the title of the slider decrease button.

### Orientation(Kendo.Mvc.UI.SliderOrientation)
Sets orientation of the slider.

### TickPlacement(Kendo.Mvc.UI.SliderTickPlacement)
Sets a value indicating how to display the tick marks on the slider.

### Min()
Sets the minimum value of the slider.

### Max()
Sets the maximum value of the slider.

### SmallStep()
Sets the step with which the slider value will change.

### LargeStep()
Sets the delta with which the value will change when user click on the slider.

### Tooltip(System.Boolean)
Display tooltip while drag.

### Tooltip(System.Action{Kendo.Mvc.UI.Fluent.SliderTooltipBuilder})
Use it to configure tooltip.

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

### Events(System.Action{Kendo.Mvc.UI.Fluent.SliderEventBuilder})
Configures the client-side events.

#### Example
    <%= Html.Kendo().Slider()
        .Name("Slider")
        .Events(events =>
        events.OnChange("onChange"))
        %>

#### Parameters

##### events `System.Action{Kendo.Mvc.UI.Fluent.SliderEventBuilder}`
The client events action.