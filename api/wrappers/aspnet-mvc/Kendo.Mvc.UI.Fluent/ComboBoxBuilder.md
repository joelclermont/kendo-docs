---
title:ComboBoxBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.comboboxbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ComboBoxBuilder

Defines the fluent interface for configuring the ComboBox component.

## Methods

### AutoBind(System.Boolean)
Controls whether to bind the widget to the DataSource on initialization.

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .AutoBind(false)
        %>

### DataValueField(System.String)
Sets the field of the data item that provides the value content of the list items.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .DataTextField("Text")
        .DataValueField("Value")
        %>

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

### Items(System.Action\<Kendo.Mvc.UI.Fluent.DropDownListItemFactory\>)
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

##### addAction `System.Action<Kendo.Mvc.UI.Fluent.DropDownListItemFactory>`
The add action.

### HighlightFirst(System.Boolean)
Use it to enable highlighting of first matched item.

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .HighlightFirst(true)
        %>

### MinLength(System.Int32)
Specifies the minimum number of characters that should be typed before the widget queries the dataSource.

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .MinLength(3)
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

### Suggest(System.Boolean)
Controls whether the ComboBox should automatically auto-type the rest of text.

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .Suggest(true)
        %>

### Placeholder(System.String)
A string that appears in the textbox when it has no value.

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .Placeholder("Select country...")
        %>

### CascadeFrom(System.String)
Use it to set the Id of the parent ComboBox.

#### Example
    <%= Html.Telerik().ComboBox()
        .Name("ComboBox2")
        .CascadeFrom("ComboBox1")
        %>

### Text(System.String)
Define the text of the widget, when the autoBind is set to false.

#### Example
    <%= Html.Telerik().ComboBox()
        .Name("ComboBox")
        .Text("Chai")
        .AutoBind(false)
        %>