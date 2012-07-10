---
title:ListViewBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.listviewbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ListViewBuilder

Defines the fluent interface for configuring the !:ListView{T}.

## Methods

### BindTo(System.Collections.Generic.IEnumerable\<T\>)
Binds the ListView to a list of objects

#### Example
    <%= Html.Kendo().ListView<Order>()
        .Name("Orders")
        .BindTo((IEnumerable<Order>)ViewData["Orders"]);
        %>

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable<T>`
The data source.

### BindTo(System.Collections.IEnumerable)
Binds the ListView to a list of objects

#### Example
    <%= Html.Kendo().ListView<Order>()
        .Name("Orders")
        .BindTo((IEnumerable)ViewData["Orders"]);
        %>

#### Parameters

##### dataSource `System.Collections.IEnumerable`
The data source.

### ClientTemplateId(System.String)
Specifies ListView item template.

#### Example
    <%= Html.Kendo().ListView<Order>()
        .Name("Orders")
        .ClientTemplateId("listViewTemplate");
        %>

#### Parameters

##### templateId `System.String`
The Id of the element which contains the template.

### Pageable
Allows paging of the data.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Ajax(ajax => ajax.Action("Orders", "ListView"))
        .Pageable();
        %>

### Pageable(System.Action\<Kendo.Mvc.UI.Fluent.PageableBuilder\>)
Allows paging of the data.

#### Example
    <%= Html.Kendo().ListView()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("Orders", "ListView"))
        .Pageable(paging => paging.Enabled(true))
        %>

#### Parameters

##### pagerAction System.Action\<[Kendo.Mvc.UI.Fluent.PageableBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/PageableBuilder)\>
Use builder to define paging settings.

### Navigatable
Enables keyboard navigation.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Ajax(ajax => ajax.Action("Orders", "ListView"))
        .Navigatable();
        %>

### Selectable
Enables single item selection.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Selectable()
        %>

### Selectable(System.Action\<Kendo.Mvc.UI.Fluent.ListViewSelectionSettingsBuilder\>)
Enables item selection.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Selectable(selection => {
        selection.Enabled(true);
        selection.Mode(ListViewSelectionMode.Multiple);
        })
        %>

#### Parameters

##### selectionAction System.Action\<[Kendo.Mvc.UI.Fluent.ListViewSelectionSettingsBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/ListViewSelectionSettingsBuilder)\>
Use builder to define the selection mode.

### TagName(System.String)
Specifies ListView wrapper element tag name.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .TagName("div")
        %>

### Editable(System.Action\<Kendo.Mvc.UI.Fluent.ListViewEditingSettingsBuilder\<T\>\>)
Configures the ListView editing settings.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Editable(settings => settings.Enabled(true))
        %>

### Editable
Enables ListView editing.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Editable()
        %>

### Events(System.Action\<Kendo.Mvc.UI.Fluent.ListViewEventBuilder\>)
Configures the client-side events.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Events(events => events
        .DataBound("onDataBound")
        )
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.ListViewEventBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/ListViewEventBuilder)\>
The client events action.