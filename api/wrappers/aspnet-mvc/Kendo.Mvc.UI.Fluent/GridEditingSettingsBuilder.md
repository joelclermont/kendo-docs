---
title:Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.grideditingsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder

## Methods

### CreateAt(Kendo.Mvc.UI.GridInsertRowPosition)
Sets insert row position.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Editable(settings => settings.CreateAt(GridInsertRowPosition.Bottom))
        %>