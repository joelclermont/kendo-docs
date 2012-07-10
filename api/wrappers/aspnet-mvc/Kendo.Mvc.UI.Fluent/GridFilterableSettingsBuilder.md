---
title:GridFilterableSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridfilterablesettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder

Defines the fluent interface for configuring Filterable.

## Methods

### Enabled(System.Boolean)
Enables or disables filtering

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Filterable(filtering => filtering.Enabled((bool)ViewData["enableFiltering"]))
        %>

### Operators(System.Action\<Kendo.Mvc.UI.Fluent.FilterableOperatorsBuilder\>)
Configures the Filter menu operators.

### Messages(System.Action\<Kendo.Mvc.UI.Fluent.FilterableMessagesBuilder\>)
Configures Filter menu messages.

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.FilterableMessagesBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/FilterableMessagesBuilder)\>

### Extra(System.Boolean)
Specify if the extra input fields should be visible within the filter menu. Default is true.

#### Parameters

##### value `System.Boolean`
True to show the extra inputs, otherwise false