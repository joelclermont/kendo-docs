---
title:Kendo.Mvc.UI.Fluent.PanelBarItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.panelbaritembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PanelBarItemBuilder

## Methods

### Items(System.Action{Kendo.Mvc.UI.Fluent.PanelBarItemFactory})
Configures the child items of a .

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.PanelBarItemFactory}`
The add action.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.PanelBarItemFactory}`
The add action.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Items(items =>
        {
        items.Add().Text("First Item").Items(firstItemChildren =>
        {
        firstItemChildren.Add().Text("Child Item 1");
        firstItemChildren.Add().Text("Child Item 2");
        });
        })
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
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
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