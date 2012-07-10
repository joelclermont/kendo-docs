---
title:MenuItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.menuitembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.MenuItemBuilder

Defines the fluent interface for configuring child menu items.

## Methods

### Items(System.Action\<Kendo.Mvc.UI.Fluent.MenuItemFactory\>)
Configures the child items of a MenuItem.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
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

##### addAction `System.Action<Kendo.Mvc.UI.Fluent.MenuItemFactory>`
The add action.