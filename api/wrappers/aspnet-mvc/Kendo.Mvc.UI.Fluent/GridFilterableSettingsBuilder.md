---
title:Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridfilterablesettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder

Defines the fluent interface for configuring .

## Methods

### Enabled(System.Boolean)
Enables or disables filtering

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Filterable(filtering => filtering.Enabled((bool)ViewData["enableFiltering"]))
        %>