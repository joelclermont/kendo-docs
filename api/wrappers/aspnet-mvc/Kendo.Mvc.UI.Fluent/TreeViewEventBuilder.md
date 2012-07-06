---
title:Kendo.Mvc.UI.Fluent.TreeViewEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treevieweventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewEventBuilder

## Methods

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