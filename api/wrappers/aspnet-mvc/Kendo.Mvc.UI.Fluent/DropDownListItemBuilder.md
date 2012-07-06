---
title:Kendo.Mvc.UI.Fluent.DropDownListItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.dropdownlistitembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.DropDownListItemBuilder

Defines the fluent interface for configuring child DropDonwList items.

## Methods

### Text(System.String)
Sets the value for the item.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Items(items => items.Add().Text("First item."))
        %>

#### Parameters

##### value `System.String`
The value.

### Value(System.String)
Sets the value for the item.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Items(items => items.Add().Value("1"))
        %>

#### Parameters

##### value `System.String`
The value.

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