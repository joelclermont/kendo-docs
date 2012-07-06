---
title:Kendo.Mvc.UI.Fluent.SliderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.sliderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SliderBuilder

## Methods

### 1.Value(System.Nullable{`0})
Sets the value of the slider.

### 1.IncreaseButtonTitle(System.String)
Sets the title of the slider increase button.

### 1.ShowButtons(System.Nullable{System.Boolean})
Sets whether slider to be rendered with increase/decrease button.

### 1.DecreaseButtonTitle(System.String)
Sets the title of the slider decrease button.

### 1.Orientation(Kendo.Mvc.UI.SliderOrientation)
Sets orientation of the slider.

### 1.TickPlacement(Kendo.Mvc.UI.SliderTickPlacement)
Sets a value indicating how to display the tick marks on the slider.

### 1.Min(`0)
Sets the minimum value of the slider.

### 1.Max(`0)
Sets the maximum value of the slider.

### 1.SmallStep(`0)
Sets the step with which the slider value will change.

### 1.LargeStep(`0)
Sets the delta with which the value will change when user click on the slider.

### 1.Tooltip(System.Boolean)
Display tooltip while drag.

### 1.Tooltip(System.Action{Kendo.Mvc.UI.Fluent.SliderTooltipBuilder})
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

### 1.Events(System.Action{Kendo.Mvc.UI.Fluent.SliderEventBuilder})
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