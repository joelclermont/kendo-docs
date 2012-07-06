---
title:Kendo.Mvc.UI.Fluent.ListViewSelectionSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.listviewselectionsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ListViewSelectionSettingsBuilder

## Methods

### Mode(Kendo.Mvc.UI.ListViewSelectionMode)
Specifies whether multiple or single selection is allowed.

#### Example
    <%= Html.Kendo().ListView(Model)
        .Name("ListView")
        .Selectable(selection => selection.Mode((bool)ViewData["selectionMode"]))
        %>