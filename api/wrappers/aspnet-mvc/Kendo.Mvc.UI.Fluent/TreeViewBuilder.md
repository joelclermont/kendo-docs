---
title:Kendo.Mvc.UI.Fluent.TreeViewBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treeviewbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewBuilder

## Methods

### DataSource(System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyDataSourceBuilder})
Configure the DataSource of the component

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataSource(dataSource => dataSource
        .Read(read => read
        .Action("Employees", "TreeView")
        )
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyDataSourceBuilder}`
The action that configures the .