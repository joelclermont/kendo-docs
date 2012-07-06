---
title:Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridfilterablesettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder

## Methods

### Enabled(System.Boolean)
Enables or disables filtering

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Filterable(filtering => filtering.Enabled((bool)ViewData["enableFiltering"]))
        %>