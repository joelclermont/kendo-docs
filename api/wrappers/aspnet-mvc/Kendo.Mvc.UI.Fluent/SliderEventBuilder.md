---
title:Kendo.Mvc.UI.Fluent.SliderEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.slidereventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SliderEventBuilder

## Methods

### Slide(System.String)
Defines the name of the JavaScript function that will handle the the Slide client-side event.

#### Example
    <%= Html.Kendo().Slider()
        .Name("Slider")
        .Events(events => events.Slide("slide"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.