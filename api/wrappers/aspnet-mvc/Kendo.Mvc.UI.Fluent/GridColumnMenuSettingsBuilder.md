---
title:Kendo.Mvc.UI.Fluent.GridColumnMenuSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridcolumnmenusettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridColumnMenuSettingsBuilder

Defines the fluent interface for configuring ColumnMenu.

## Methods

### Enabled(System.Boolean)
Enables/disables header column menu.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .ColumnMenu(menu => menu.Enabled((bool)ViewData["enableColumnMenu"]))
        %>

### Sortable(System.Boolean)
Enables/disables sort section in header column menu.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .ColumnMenu(menu => menu.Sortable((bool)ViewData["enableSort"]))
        %>

### Filterable(System.Boolean)
Enables/disables filter section in header column menu.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .ColumnMenu(menu => menu.Filterable((bool)ViewData["enableFilter"]))
        %>

### Columns(System.Boolean)
Enables/disables columns section in header column menu.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .ColumnMenu(menu => menu.Columns((bool)ViewData["enableColumns"]))
        %>

### Messages(System.Action{Kendo.Mvc.UI.Fluent.ColumnMenuMessagesBuilder})
Enables you to define custom messages in grid column menu.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .ColumnMenu(menu => menu.Messages(msg => msg.Filter("Custom filter message"))
        %>