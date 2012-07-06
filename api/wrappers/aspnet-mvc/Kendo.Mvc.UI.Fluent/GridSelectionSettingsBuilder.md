---
title:Kendo.Mvc.UI.Fluent.GridSelectionSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridselectionsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridSelectionSettingsBuilder

## Methods

### Type(Kendo.Mvc.UI.GridSelectionType)
Specifies whether row or cell selection is allowed.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Selectable(selection => selection.Type((bool)ViewData["selectionType"]))
        %>