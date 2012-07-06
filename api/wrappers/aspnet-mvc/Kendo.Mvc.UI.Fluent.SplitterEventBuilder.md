---
title:Kendo.Mvc.UI.Fluent.SplitterEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.splittereventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SplitterEventBuilder

## Methods

### Resize(System.Func{System.Object,System.Object})
Defines the inline handler of the Resize client-side event

#### Parameters

##### onResizeInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onResizeInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.Resize(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### Resize(System.String)
Defines the name of the JavaScript function that will handle the the Resize client-side event.

#### Parameters

##### onResizeHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onResizeHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.Resize("onResize"))
        %>

### Expand(System.Func{System.Object,System.Object})
Defines the inline handler of the Expand client-side event

#### Parameters

##### onExpandInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onExpandInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().Splitter()
        .Name("Splitter")
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

##### onExpandHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onExpandHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.Expand("onExpand"))
        %>

### Collapse(System.Func{System.Object,System.Object})
Defines the inline handler of the Collapse client-side event

#### Parameters

##### onCollapseInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onCollapseInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().Splitter()
        .Name("Splitter")
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

##### onCollapseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onCollapseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.Collapse("onCollapse"))
        %>

### ContentLoad(System.Func{System.Object,System.Object})
Defines the inline handler of the ContentLoad client-side event

#### Parameters

##### onContentLoadInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onContentLoadInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().Splitter()
        .Name("Splitter")
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

##### onContentLoadHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onContentLoadHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.ContentLoad("onContentLoad"))
        %>