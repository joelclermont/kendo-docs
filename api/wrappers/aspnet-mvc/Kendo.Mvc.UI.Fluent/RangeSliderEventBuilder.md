---
title:Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.rangeslidereventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder

## Methods

### Slide(System.String)
Defines the name of the JavaScript function that will handle the the Slide client-side event.

#### Example
    <%= Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        .Events(events => events.Slide("slide"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.