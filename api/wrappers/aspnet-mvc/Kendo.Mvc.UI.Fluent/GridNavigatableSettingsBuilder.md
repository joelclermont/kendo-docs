---
title:Kendo.Mvc.UI.Fluent.GridNavigatableSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridnavigatablesettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridNavigatableSettingsBuilder

Defines the fluent interface for configuring

## Methods

### Enabled(System.Boolean)
Enables or disables keyboard navigation.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Navigatable(setting => setting.Enabled((bool)ViewData["enableKeyBoardNavigation"]))
        %>