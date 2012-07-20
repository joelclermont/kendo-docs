---
title:DropDownListBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.dropdownlistbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.DropDownListBuilder

Defines the fluent interface for configuring the DropDownList component.

## Methods

### DataValueField(System.String)
Sets the field of the data item that provides the value content of the list items.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .DataTextField("Text")
        .DataValueField("Value")
        %>

### Items(System.Action\<Kendo.Mvc.UI.Fluent.DropDownListItemFactory\>)
Defines the items in the DropDownList

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

#### Parameters

##### addAction System.Action\<[Kendo.Mvc.UI.Fluent.DropDownListItemFactory](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/DropDownListItemFactory)\>
The add action.

### OptionLabel(System.String)
Define the text of the default empty item. If the value is an object, then the widget will use it directly.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .OptionLabel("Select country...")
        %>

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

### CascadeFrom(System.String)
Use it to set the Id of the parent DropDownList.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList2")
        .CascadeFrom("DropDownList1")
        %>

### Text(System.String)
Define the text of the widget, when the autoBind is set to false.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Text("Chai")
        .AutoBind(false)
        %>
