---
title:Kendo.Mvc.UI.Fluent.MenuItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.menuitembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.MenuItemBuilder

## Methods

### Items(System.Action{Kendo.Mvc.UI.Fluent.MenuItemFactory})
Configures the child items of a .

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.MenuItemFactory}`
The add action.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.MenuItemFactory}`
The add action.

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