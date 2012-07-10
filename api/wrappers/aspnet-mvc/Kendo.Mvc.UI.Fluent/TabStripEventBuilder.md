---
title:TabStripEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.tabstripeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TabStripEventBuilder

Defines the fluent interface for configuring the Events.

## Methods

### Activate(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Activate client-side event

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

#### Parameters

##### onSelectAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Activate(System.String)
Defines the name of the JavaScript function that will handle the the Activate client-side event.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.Activate("onActivate"))
        %>

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Select(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Select client-side event

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

#### Parameters

##### onSelectAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.Select("onSelect"))
        %>

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### ContentLoad(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the ContentLoad client-side event

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

#### Parameters

##### onSelectAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### ContentLoad(System.String)
Defines the name of the JavaScript function that will handle the the ContentLoad client-side event.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.ContentLoad("onContentLoad"))
        %>

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Error(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Error client-side event

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

#### Parameters

##### onErrorAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events => events.Error("onError"))
        %>

#### Parameters

##### onErrorHandlerName `System.String`
The name of the JavaScript function that will handle the event.