---
title:Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.grideditingsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder

## Methods

### 1.Enabled(System.Boolean)
Enables or disables grid editing.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Editable(settings => settings.Enabled(true))
        %>

### 1.TemplateName(System.String)
Specify an editor template which to be used for InForm or PopUp modes

#### Parameters

##### templateName `System.String`
name of the editor template

#### Parameters

##### templateName `System.String`
name of the editor template

### 1.AdditionalViewData(System.Object)
Provides additional view data in the editor template.

#### Parameters

##### additionalViewData `System.Object`
An anonymous object which contains the additional data

#### Parameters

##### additionalViewData `System.Object`
An anonymous object which contains the additional data

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Editable(editing => editing.AdditionalViewData(new { customers = Model.Customers }))
        %>

### 1.DisplayDeleteConfirmation(System.Boolean)
Enables or disables delete confirmation.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Editable(settings => settings.DisplayDeleteConfirmation(true))
        %>

### 1.CreateAt(Kendo.Mvc.UI.GridInsertRowPosition)
Sets insert row position.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Editable(settings => settings.CreateAt(GridInsertRowPosition.Bottom))
        %>