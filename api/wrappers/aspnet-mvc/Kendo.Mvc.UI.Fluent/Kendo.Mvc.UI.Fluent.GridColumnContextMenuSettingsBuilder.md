---
title:Kendo.Mvc.UI.Fluent.GridColumnContextMenuSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridcolumncontextmenusettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridColumnContextMenuSettingsBuilder

## Methods

### Enabled(System.Boolean)
Enables or disables column context menu.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .ColumnContextMenu(setting => setting.Enabled((bool)ViewData["enableColumnContextMenu"]))
        %>