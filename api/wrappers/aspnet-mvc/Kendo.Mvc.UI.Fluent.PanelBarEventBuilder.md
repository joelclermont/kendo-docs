---
title:Kendo.Mvc.UI.Fluent.PanelBarEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.panelbareventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PanelBarEventBuilder

## Methods

### Expand(System.Func{System.Object,System.Object})
Defines the inline handler of the Expand client-side event

#### Parameters

##### expandInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### expandInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Expand(System.String)
Defines the name of the JavaScript function that will handle the the Expand client-side event.

#### Parameters

##### expandHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### expandHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Expand("expand"))
        %>

### ContentLoad(System.Func{System.Object,System.Object})
Defines the inline handler of the ContentLoad client-side event

#### Parameters

##### contentLoadInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### contentLoadInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### ContentLoad(System.String)
Defines the name of the JavaScript function that will handle the the ContentLoad client-side event.

#### Parameters

##### contentLoadHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### contentLoadHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.ContentLoad("contentLoad"))
        %>

### Collapse(System.Func{System.Object,System.Object})
Defines the inline handler of the Collapse client-side event

#### Parameters

##### collapseInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### collapseInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Collapse(System.String)
Defines the name of the JavaScript function that will handle the the Collapse client-side event.

#### Parameters

##### collapseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### collapseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Collapse("collapse"))
        %>

### Select(System.Func{System.Object,System.Object})
Defines the inline handler of the Select client-side event

#### Parameters

##### selectInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### selectInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Parameters

##### selectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### selectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Select("select"))
        %>

### Error(System.Func{System.Object,System.Object})
Defines the inline handler of the Error client-side event

#### Parameters

##### errorInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### errorInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Parameters

##### errorHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### errorHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events => events.Error("onError"))
        %>