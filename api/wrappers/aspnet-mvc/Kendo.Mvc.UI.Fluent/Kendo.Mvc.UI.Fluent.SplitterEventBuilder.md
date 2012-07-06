---
title:Kendo.Mvc.UI.Fluent.SplitterEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.splittereventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SplitterEventBuilder

## Methods

### Resize(System.Func{System.Object,System.Object})
Defines the inline handler of the Resize client-side event

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

#### Parameters

##### onResizeInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

### Resize(System.String)
Defines the name of the JavaScript function that will handle the the Resize client-side event.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.Resize("onResize"))
        %>

#### Parameters

##### onResizeHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Expand(System.Func{System.Object,System.Object})
Defines the inline handler of the Expand client-side event

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

#### Parameters

##### onExpandInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

### Expand(System.String)
Defines the name of the JavaScript function that will handle the the Expand client-side event.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.Expand("onExpand"))
        %>

#### Parameters

##### onExpandHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Collapse(System.Func{System.Object,System.Object})
Defines the inline handler of the Collapse client-side event

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

#### Parameters

##### onCollapseInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

### Collapse(System.String)
Defines the name of the JavaScript function that will handle the the Collapse client-side event.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.Collapse("onCollapse"))
        %>

#### Parameters

##### onCollapseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### ContentLoad(System.Func{System.Object,System.Object})
Defines the inline handler of the ContentLoad client-side event

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

#### Parameters

##### onContentLoadInlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

### ContentLoad(System.String)
Defines the name of the JavaScript function that will handle the the ContentLoad client-side event.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.ContentLoad("onContentLoad"))
        %>

#### Parameters

##### onContentLoadHandlerName `System.String`
The name of the JavaScript function that will handle the event.