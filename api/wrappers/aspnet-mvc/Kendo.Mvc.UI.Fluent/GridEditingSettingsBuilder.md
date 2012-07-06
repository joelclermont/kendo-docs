---
title:Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.grideditingsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder

Defines the fluent interface for configuring grid editing.

## Methods

### Enabled(System.Boolean)
Enables or disables grid editing.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Editable(settings => settings.Enabled(true))
        %>

### TemplateName(System.String)
Specify an editor template which to be used for InForm or PopUp modes

#### Parameters

##### templateName `System.String`
name of the editor template

### AdditionalViewData(System.Object)
Provides additional view data in the editor template.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Editable(editing => editing.AdditionalViewData(new { customers = Model.Customers }))
        %>

#### Parameters

##### additionalViewData `System.Object`
An anonymous object which contains the additional data

### DisplayDeleteConfirmation(System.Boolean)
Enables or disables delete confirmation.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Editable(settings => settings.DisplayDeleteConfirmation(true))
        %>

### CreateAt(Kendo.Mvc.UI.GridInsertRowPosition)
Sets insert row position.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Editable(settings => settings.CreateAt(GridInsertRowPosition.Bottom))
        %>