---
title:Kendo.Mvc.UI.Fluent.TreeViewBindingSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treeviewbindingsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewBindingSettingsBuilder

## Methods

### Select(System.String)
Sets the route name for the select operation

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataBinding(dataBinding =>
        {
        dataBinding.Ajax().Select("Default");
        })
        %>

#### Parameters

##### routeName `System.String`
Name of the route.