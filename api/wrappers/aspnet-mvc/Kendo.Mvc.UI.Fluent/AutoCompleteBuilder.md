---
title:Kendo.Mvc.UI.Fluent.AutoCompleteBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.autocompletebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.AutoCompleteBuilder

Defines the fluent interface for configuring the AutoComplete component.

## Methods

### Filter(System.String)
Use it to enable filtering of items.

#### Example
    <%= Html.Kendo().AutoComplete()
        .Name("AutoComplete")
        .Filter("startswith");
        %>

### Filter(Kendo.Mvc.UI.FilterType)
Use it to enable filtering of items.

#### Example
    <%= Html.Kendo().AutoComplete()
        .Name("AutoComplete")
        .Filter(FilterType.Contains);
        %>

### HighlightFirst(System.Boolean)
Use it to enable highlighting of first matched item.

#### Example
    <%= Html.Kendo().AutoComplete()
        .Name("AutoComplete")
        .HighlightFirst(true)
        %>

### MinLength(System.Int32)
Specifies the minimum number of characters that should be typed before the widget queries the dataSource.

#### Example
    <%= Html.Kendo().AutoComplete()
        .Name("AutoComplete")
        .MinLength(3)
        %>

### Placeholder(System.String)
A string that appears in the textbox when it has no value.

#### Example
    <%= Html.Kendo().AutoComplete()
        .Name("AutoComplete")
        .MinLength(3)
        %>

### Separator(System.String)
Sets the separator for completion. Empty by default, allowing for only one completion.

#### Example
    <%= Html.Kendo().AutoComplete()
        .Name("AutoComplete")
        .Separator(", ")
        %>

### Suggest(System.Boolean)
Controls whether the AutoComplete should automatically auto-type the rest of text.

#### Example
    <%= Html.Kendo().AutoComplete()
        .Name("AutoComplete")
        .Suggest(true)
        %>