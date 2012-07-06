---
title:Kendo.Mvc.UI.Fluent.SliderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.sliderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SliderBuilder

## Methods

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