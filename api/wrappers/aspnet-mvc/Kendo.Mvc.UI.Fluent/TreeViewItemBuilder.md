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

##### addAction System.Action\<[Kendo.Mvc.UI.Fluent.TreeViewItemFactory](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/TreeViewItemFactory)\>
The add action.

### Id(System.String)
Sets the id of the item.

#### Example
    <%= Html.Telerik().TreeView()
        .Name("TreeView")
        .Items(items => items.Add().Id("42"))
        %>

#### Parameters

##### value `System.String`
The id.

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

### HasChildren(System.Boolean)
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
        .HasChildren(true);
        })
        %>

#### Parameters

##### value `System.Boolean`
If true then item will be loaded on demand from client side, if the treeview DataSource is properly configured.