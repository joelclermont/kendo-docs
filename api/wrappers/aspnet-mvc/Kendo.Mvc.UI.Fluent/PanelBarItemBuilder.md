---
title:PanelBarItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.panelbaritembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PanelBarItemBuilder

Defines the fluent interface for configuring child panelbar items.

## Methods

### Items(System.Action\<Kendo.Mvc.UI.Fluent.PanelBarItemFactory\>)
Configures the child items of a PanelBarItem.

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

#### Parameters

##### addAction `System.Action<Kendo.Mvc.UI.Fluent.PanelBarItemFactory>`
The add action.

### Expanded(System.Boolean)
Define when the item will be expanded on intial render.

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

#### Parameters

##### value `System.Boolean`
If true the item will be expanded.