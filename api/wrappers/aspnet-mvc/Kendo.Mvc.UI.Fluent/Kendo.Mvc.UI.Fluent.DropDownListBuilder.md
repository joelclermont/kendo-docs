---
title:Kendo.Mvc.UI.Fluent.DropDownListBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.dropdownlistbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.DropDownListBuilder

## Methods

### Items(System.Action{Kendo.Mvc.UI.Fluent.DropDownListItemFactory})
Defines the items in the DropDownList

#### Example
    <%= Html.Telerik().DropDownList()
        .Name("DropDownList")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.DropDownListItemFactory}`
The add action.

### SelectedIndex(System.Int32)
Use it to set selected item index

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .SelectedIndex(0);
        %>

#### Parameters

##### index `System.Int32`
Item index.