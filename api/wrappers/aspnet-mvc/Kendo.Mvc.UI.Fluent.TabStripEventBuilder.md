---
title:Kendo.Mvc.UI.Fluent.TabStripEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.tabstripeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TabStripEventBuilder

## Methods

### Activate(System.Func{System.Object,System.Object})
Defines the inline handler of the Activate client-side event

#### Parameters

##### onSelectAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onSelectAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.Activate(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### Activate(System.String)
Defines the name of the JavaScript function that will handle the the Activate client-side event.

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.Activate("onActivate"))
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
    <% Html.Kendo().TabStrip()
        .Name("TabStrip")
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
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.Select("onSelect"))
        %>

### ContentLoad(System.Func{System.Object,System.Object})
Defines the inline handler of the ContentLoad client-side event

#### Parameters

##### onSelectAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onSelectAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.ContentLoad(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### ContentLoad(System.String)
Defines the name of the JavaScript function that will handle the the ContentLoad client-side event.

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.ContentLoad("onContentLoad"))
        %>

### Error(System.Func{System.Object,System.Object})
Defines the inline handler of the Error client-side event

#### Parameters

##### onErrorAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onErrorAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.Error(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Parameters

##### onErrorHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onErrorHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.Error("onError"))
        %>