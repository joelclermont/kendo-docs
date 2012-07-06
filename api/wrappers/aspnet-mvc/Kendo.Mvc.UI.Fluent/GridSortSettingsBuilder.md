---
title:Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridsortsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder

Defines the fluent interface for configuring the .

## Methods

### Enabled(System.Boolean)
Enables or disables sorting.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Sorting(sorting => sorting.Enabled((bool)ViewData["enableSorting"]))
        %>

### SortMode(Kendo.Mvc.UI.GridSortMode)
Sets the sort mode of the grid.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Sorting(sorting => sorting.SortMode(GridSortMode.MultipleColumns))
        %>

#### Parameters

##### value `Kendo.Mvc.UI.GridSortMode`
The value.

### AllowUnsort(System.Boolean)
Enables or disables unsorted mode.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Sorting(sorting => sorting.AllowUnsort(true))
        %>

#### Parameters

##### value `System.Boolean`
The value.