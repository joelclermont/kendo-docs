---
title:Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.rangeslidereventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.RangeSliderEventBuilder

## Methods

### Change(System.Func{System.Object,System.Object})
Defines the inline handler of the Change client-side event

#### Parameters

##### handlerName `System.Func{System.Object`
The action defining the inline handler.

#### Parameters

##### handlerName `System.Func{System.Object`
The action defining the inline handler.

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

### Change(System.String)
Defines the name of the JavaScript function that will handle the the Kendo client-side event.

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        .Events(events => events.Change("change"))
        %>

### Slide(System.Func{System.Object,System.Object})
Defines the inline handler of the Slide client-side event.

#### Parameters

##### handlerName `System.Func{System.Object`
The action defining the inline handler.

#### Parameters

##### handlerName `System.Func{System.Object`
The action defining the inline handler.

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

### Slide(System.String)
Defines the name of the JavaScript function that will handle the the Slide client-side event.

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        .Events(events => events.Slide("slide"))
        %>