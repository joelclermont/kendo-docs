---
title:Kendo.Mvc.UI.Fluent.TreeViewEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treevieweventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewEventBuilder

## Methods

### Expand(System.Func{System.Object,System.Object})
Defines the inline handler of the Expand client-side event

#### Parameters

##### onExpandAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onExpandAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Expand(
        @<text>
        function(e) {
        // event handling code
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
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Expand("onExpand"))
        %>

### Collapse(System.Func{System.Object,System.Object})
Defines the inline handler of the Collapse client-side event

#### Parameters

##### onCollapseAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onCollapseAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Collapse(
        @<text>
        function(e) {
        // event handling code
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
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Collapse("onCollapse"))
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
    <% Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Select(
        @<text>
        function(e) {
        // event handling code
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
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Select("onSelect"))
        %>

### DragStart(System.Func{System.Object,System.Object})
Defines the inline handler of the DragStart client-side event

#### Parameters

##### onNodeDragAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onNodeDragAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.DragStart(
        @<text>
        function(e) {
        // event handling code
        }
        </text>
        ))
        .Render();
        %>

### DragStart(System.String)
Defines the name of the JavaScript function that will handle the the DragStart client-side event.

#### Parameters

##### onNodeDragHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onNodeDragHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.DragStart("onNodeDragStrat"))
        %>

### Drop(System.String)
Defines the name of the JavaScript function that will handle the the Drop client-side event.

#### Parameters

##### DropHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### DropHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Drop("Drop"))
        %>

### DragEnd(System.Func{System.Object,System.Object})
Defines the inline handler of the DragEnd client-side event

#### Parameters

##### DragEndAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### DragEndAction `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.DragEnd(
        @<text>
        function(e) {
        // event handling code
        }
        </text>
        ))
        .Render();
        %>

### DragEnd(System.String)
Defines the name of the JavaScript function that will handle the the DragEnd client-side event.

#### Parameters

##### DragEndHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### DragEndHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.DragEnd("DragEnd"))
        %>

### Drag(System.Func{System.Object,System.Object})
Defines the inline handler of the Drag client-side event

#### Parameters

##### onNodeDragging `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### onNodeDragging `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Drag(
        @<text>
        function(e) {
        // event handling code
        }
        </text>
        ))
        .Render();
        %>

### Drag(System.String)
Defines the name of the JavaScript function that will handle the the Drag client-side event.

#### Parameters

##### onNodeDragging `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onNodeDragging `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Drag("Drag"))
        %>