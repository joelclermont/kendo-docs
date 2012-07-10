---
title:PanelBarEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.panelbareventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PanelBarEventBuilder

Defines the fluent interface for configuring the Events.

## Methods

### Expand(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Expand client-side event

#### Example
    <% Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Expand(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

#### Parameters

##### expandInlineCodeBlock `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Expand(System.String)
Defines the name of the JavaScript function that will handle the the Expand client-side event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Expand("expand"))
        %>

#### Parameters

##### expandHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### ContentLoad(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the ContentLoad client-side event

#### Example
    <% Html.Kendo().PanelBar()
        .Name("PanelBar")
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

##### contentLoadInlineCodeBlock `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### ContentLoad(System.String)
Defines the name of the JavaScript function that will handle the the ContentLoad client-side event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.ContentLoad("contentLoad"))
        %>

#### Parameters

##### contentLoadHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Collapse(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Collapse client-side event

#### Example
    <% Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Collapse(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

#### Parameters

##### collapseInlineCodeBlock `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Collapse(System.String)
Defines the name of the JavaScript function that will handle the the Collapse client-side event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Collapse("collapse"))
        %>

#### Parameters

##### collapseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Select(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Select client-side event

#### Example
    <% Html.Kendo().PanelBar()
        .Name("PanelBar")
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

##### selectInlineCodeBlock `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Select("select"))
        %>

#### Parameters

##### selectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Error(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Error client-side event

#### Example
    <% Html.Kendo().PanelBar()
        .Name("PanelBar")
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

##### errorInlineCodeBlock `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Error("onError"))
        %>

#### Parameters

##### errorHandlerName `System.String`
The name of the JavaScript function that will handle the event.