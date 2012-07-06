---
title:Kendo.Mvc.UI.Fluent.TreeViewItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treeviewitembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewItemBuilder

## Methods

### LoadOnDemand(System.Boolean)
Sets the expand mode of the treeview item.

#### Example
    <%= Html.Telerik().TreeView()
        .Name("TreeView")
        .Items(items =>
        {
        items.Add().Text("First Item").Items(firstItemChildren =>
        {
        firstItemChildren.Add().Text("Child Item 1");
        firstItemChildren.Add().Text("Child Item 2");
        })
        .LoadOnDemand(true);
        })
        %>

#### Parameters

##### value `System.Boolean`
If true then item will be load on demand from client side.