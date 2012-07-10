---
title:RangeSliderEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.rangeslidereventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder

Defines the fluent interface for configuring the RangeSlider events.

## Methods

### Change(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Change client-side event

#### Example
    <% Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        .Events(events => events.Change(() =>
        {
        %>
        function(e) {
        //event handling code
        }
        <%
        }))
        .Render();
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The action defining the inline handler.

### Change(System.String)
Defines the name of the JavaScript function that will handle the the Kendo client-side event.

#### Example
    <%= Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        .Events(events => events.Change("change"))
        %>

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

### Slide(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Slide client-side event.

#### Example
    <% Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        .Events(events => events.Slide(() =>
        {
        %>
        function(e) {
        //event handling code
        }
        <%
        }))
        .Render();
        %>

#### Parameters

##### handlerName `System.Func<System.Object,System.Object>`
The action defining the inline handler.

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