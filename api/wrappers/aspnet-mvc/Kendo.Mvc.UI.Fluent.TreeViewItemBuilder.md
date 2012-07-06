---
title:Kendo.Mvc.UI.Fluent.TreeViewItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treeviewitembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewItemBuilder

## Methods

### Items(System.Action{Kendo.Mvc.UI.Fluent.TreeViewItemFactory})
Configures the child items of a .

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.TreeViewItemFactory}`
The add action.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.TreeViewItemFactory}`
The add action.

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

### Value(System.String)
Sets the value for the item.

#### Parameters

##### value `System.String`
The value.

#### Parameters

##### value `System.String`
The value.

#### Example
    <%= Html.Telerik().TreeView()
        .Name("TreeView")
        .Items(items => items.Add().Value("1"))
        %>

### Expanded(System.Boolean)
Define when the item will be expanded on intial render.

#### Parameters

##### value `System.Boolean`
If true the item will be expanded.

#### Parameters

##### value `System.Boolean`
If true the item will be expanded.

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

### Checked(System.Boolean)
Define when the item will be checked on intial render.

#### Parameters

##### value `System.Boolean`
If true the item will be checked.

#### Parameters

##### value `System.Boolean`
If true the item will be checked.

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

### Checkable(System.Boolean)
Enables/disables the rendering of a checkbox for this item.

#### Parameters

##### value `System.Boolean`
If false, no checkbox will be rendered.

#### Parameters

##### value `System.Boolean`
If false, no checkbox will be rendered.

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

### LoadOnDemand(System.Boolean)
Sets the expand mode of the treeview item.

#### Parameters

##### value `System.Boolean`
If true then item will be load on demand from client side.

#### Parameters

##### value `System.Boolean`
If true then item will be load on demand from client side.

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