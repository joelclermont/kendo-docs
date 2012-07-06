---
title:Kendo.Mvc.UI.Fluent.PanelBarItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.panelbaritembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PanelBarItemBuilder

## Methods

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