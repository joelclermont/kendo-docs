---
title:Kendo.Mvc.UI.Fluent.MenuEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.menueventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.MenuEventBuilder

## Methods

### Open(System.Func{System.Object,System.Object})
Defines the inline handler of the Open client-side event

#### Parameters

##### onOpenAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onOpenAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Open(System.String)
Defines the name of the JavaScript function that will handle the the Open client-side event.

#### Parameters

##### onOpenHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onOpenHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Open("onOpen"))
        %>

### Close(System.Func{System.Object,System.Object})
Defines the inline handler of the Close client-side event

#### Parameters

##### onCloseAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onCloseAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Close(System.String)
Defines the name of the JavaScript function that will handle the the Close client-side event.

#### Parameters

##### onCloseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onCloseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Close("onClose"))
        %>

### Select(System.Func{System.Object,System.Object})
Defines the inline handler of the Select client-side event

#### Parameters

##### onSelectAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onSelectAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Events(events => events.Select("onSelect"))
        %>