---
title:Kendo.Mvc.UI.Fluent.RangeSliderBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.rangesliderbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.RangeSliderBuilder

## Methods

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