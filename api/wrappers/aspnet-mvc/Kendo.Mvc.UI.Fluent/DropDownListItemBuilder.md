---
title:Kendo.Mvc.UI.Fluent.DropDownListItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.dropdownlistitembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.DropDownListItemBuilder

## Methods

### Selected(System.Boolean)
Define when the item will be expanded on intial render.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Items(items =>
        {
        items.Add().Text("First Item").Selected(true);
        })
        %>

#### Parameters

##### value `System.Boolean`
If true the item will be selected.