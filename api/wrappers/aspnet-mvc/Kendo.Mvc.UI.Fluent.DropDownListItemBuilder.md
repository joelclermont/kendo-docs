---
title:Kendo.Mvc.UI.Fluent.DropDownListItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.dropdownlistitembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.DropDownListItemBuilder

## Methods

### Text(System.String)
Sets the value for the item.

#### Parameters

##### value `System.String`
The value.

#### Parameters

##### value `System.String`
The value.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Items(items => items.Add().Text("First item."))
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
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Items(items => items.Add().Value("1"))
        %>

### Selected(System.Boolean)
Define when the item will be expanded on intial render.

#### Parameters

##### value `System.Boolean`
If true the item will be selected.

#### Parameters

##### value `System.Boolean`
If true the item will be selected.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Items(items =>
        {
        items.Add().Text("First Item").Selected(true);
        })
        %>