---
title:Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridsortsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder

## Methods

### 1.Enabled(System.Boolean)
Enables or disables sorting.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Sorting(sorting => sorting.Enabled((bool)ViewData["enableSorting"]))
        %>

### 1.SortMode(Kendo.Mvc.UI.GridSortMode)
Sets the sort mode of the grid.

#### Parameters

##### value `Kendo.Mvc.UI.GridSortMode`
The value.

#### Parameters

##### value `Kendo.Mvc.UI.GridSortMode`
The value.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Sorting(sorting => sorting.SortMode(GridSortMode.MultipleColumns))
        %>

### 1.AllowUnsort(System.Boolean)
Enables or disables unsorted mode.

#### Parameters

##### value `System.Boolean`
The value.

#### Parameters

##### value `System.Boolean`
The value.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Sorting(sorting => sorting.AllowUnsort(true))
        %>