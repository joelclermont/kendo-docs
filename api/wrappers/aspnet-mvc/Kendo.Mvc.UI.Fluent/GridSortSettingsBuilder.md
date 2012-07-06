---
title:Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridsortsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder

## Methods

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