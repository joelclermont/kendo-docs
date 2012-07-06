---
title:Kendo.Mvc.UI.Fluent.AutoCompleteBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.autocompletebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.AutoCompleteBuilder

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