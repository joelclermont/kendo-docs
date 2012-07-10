---
title:MenuEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.menueventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.MenuEventBuilder

Defines the fluent interface for configuring the Events.

## Methods

### Open(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Open client-side event

#### Example
    <% Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Open(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

#### Parameters

##### onOpenAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Open(System.String)
Defines the name of the JavaScript function that will handle the the Open client-side event.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Open("onOpen"))
        %>

#### Parameters

##### onOpenHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Close(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Close client-side event

#### Example
    <% Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Close(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

#### Parameters

##### onCloseAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Close(System.String)
Defines the name of the JavaScript function that will handle the the Close client-side event.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Close("onClose"))
        %>

#### Parameters

##### onCloseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Select(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Select client-side event

#### Example
    <% Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Select(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

#### Parameters

##### onSelectAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Select("onSelect"))
        %>

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.