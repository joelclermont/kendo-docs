---
title:ListViewSelectionSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.listviewselectionsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ListViewSelectionSettingsBuilder

Defines the fluent interface for configuring Selection

## Methods

### Enabled(System.Boolean)
Enables or disables selection.

#### Example
    <%= Html.Kendo().ListView(Model)
        .Name("ListView")
        .Selectable(selection => selection.Enabled((bool)ViewData["enableSelection"]))
        %>

### Mode(Kendo.Mvc.UI.ListViewSelectionMode)
Specifies whether multiple or single selection is allowed.

#### Example
    <%= Html.Kendo().ListView(Model)
        .Name("ListView")
        .Selectable(selection => selection.Mode((bool)ViewData["selectionMode"]))
        %>