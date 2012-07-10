---
title:TreeViewItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treeviewitembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewItemBuilder

Defines the fluent interface for configuring child TreeView items.

## Methods

### Items(System.Action\<Kendo.Mvc.UI.Fluent.TreeViewItemFactory\>)
Configures the child items of a TreeViewItem.

#### Example
    <%= Html.Telerik().TreeView()
        .Name("TreeView")
        .Items(items =>
        {
        items.Add().Text("First Item").Items(firstItemChildren =>
        {
        firstItemChildren.Add().Text("Child Item 1");
        firstItemChildren.Add().Text("Child Item 2");
        });
        })
        %>

#### Parameters

##### addAction `System.Action<Kendo.Mvc.UI.Fluent.TreeViewItemFactory>`
The add action.

### Value(System.String)
Sets the value for the item.

#### Example
    <%= Html.Telerik().TreeView()
        .Name("TreeView")
        .Items(items => items.Add().Value("1"))
        %>

#### Parameters

##### value `System.String`
The value.

### Expanded(System.Boolean)
Define when the item will be expanded on intial render.

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
        .Expanded(true);
        })
        %>

#### Parameters

##### value `System.Boolean`
If true the item will be expanded.

### Checked(System.Boolean)
Define when the item will be checked on intial render.

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
        .Checked(true);
        })
        %>

#### Parameters

##### value `System.Boolean`
If true the item will be checked.

### Checkable(System.Boolean)
Enables/disables the rendering of a checkbox for this item.

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
        .Checkable(false);
        })
        %>

#### Parameters

##### value `System.Boolean`
If false, no checkbox will be rendered.

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