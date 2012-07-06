---
title:Kendo.Mvc.UI.Fluent.ComboBoxBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.comboboxbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ComboBoxBuilder

Defines the fluent interface for configuring the  component.

## Methods

### Filter(System.String)
Use it to enable filtering of items.

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .Filter("startswith");
        %>

### Filter(Kendo.Mvc.UI.FilterType)
Use it to enable filtering of items.

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .Filter(FilterType.Contains);
        %>

### Items(System.Action{Kendo.Mvc.UI.Fluent.DropDownListItemFactory})
Defines the items in the ComboBox

#### Example
    <%= Html.Telerik().ComboBox()
        .Name("ComboBox")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.DropDownListItemFactory}`
The add action.

### HighlightFirst(System.Boolean)
Use it to enable highlighting of first matched item.

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .HighlightFirst(true)
        %>

### SelectedIndex(System.Int32)
Use it to set selected item index

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .SelectedIndex(0);
        %>

#### Parameters

##### index `System.Int32`
Item index.