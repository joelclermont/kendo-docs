---
title:TreeViewEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treevieweventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewEventBuilder

Defines the fluent API for configuring the Kendo TreeView for ASP.NET MVC events

## Methods

### Expand(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Expand client-side event

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

#### Parameters

##### onExpandAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Expand(System.String)
Defines the name of the JavaScript function that will handle the the Expand client-side event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Expand("onExpand"))
        %>

#### Parameters

##### onExpandHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Collapse(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Collapse client-side event

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

#### Parameters

##### onCollapseAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Collapse(System.String)
Defines the name of the JavaScript function that will handle the the Collapse client-side event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Collapse("onCollapse"))
        %>

#### Parameters

##### onCollapseHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Select(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Select client-side event

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

#### Parameters

##### onSelectAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Select("onSelect"))
        %>

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### DragStart(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the DragStart client-side event

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

#### Parameters

##### onNodeDragAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### DragStart(System.String)
Defines the name of the JavaScript function that will handle the the DragStart client-side event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.DragStart("onNodeDragStrat"))
        %>

#### Parameters

##### onNodeDragHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Drop(System.String)
Defines the name of the JavaScript function that will handle the the Drop client-side event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Drop("Drop"))
        %>

#### Parameters

##### DropHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### DragEnd(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the DragEnd client-side event

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

#### Parameters

##### DragEndAction `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### DragEnd(System.String)
Defines the name of the JavaScript function that will handle the the DragEnd client-side event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.DragEnd("DragEnd"))
        %>

#### Parameters

##### DragEndHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Drag(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Drag client-side event

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

#### Parameters

##### onNodeDragging `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Drag(System.String)
Defines the name of the JavaScript function that will handle the the Drag client-side event.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events => events.Drag("Drag"))
        %>

#### Parameters

##### onNodeDragging `System.String`
The name of the JavaScript function that will handle the event.