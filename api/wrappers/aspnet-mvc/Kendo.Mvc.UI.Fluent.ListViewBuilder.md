---
title:Kendo.Mvc.UI.Fluent.ListViewBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.listviewbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ListViewBuilder

## Methods

### 1.BindTo(System.Collections.Generic.IEnumerable{`0})
Binds the ListView to a list of objects

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{`0}`
The data source.

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{`0}`
The data source.

#### Example
    <%= Html.Kendo().ListView<Order>()
        .Name("Orders")
        .BindTo((IEnumerable<Order>)ViewData["Orders"]);
        %>

### 1.BindTo(System.Collections.IEnumerable)
Binds the ListView to a list of objects

#### Parameters

##### dataSource `System.Collections.IEnumerable`
The data source.

#### Parameters

##### dataSource `System.Collections.IEnumerable`
The data source.

#### Example
    <%= Html.Kendo().ListView<Order>()
        .Name("Orders")
        .BindTo((IEnumerable)ViewData["Orders"]);
        %>

### 1.ClientTemplateId(System.String)
Specifies ListView item template.

#### Parameters

##### templateId `System.String`
The Id of the element which contains the template.

#### Parameters

##### templateId `System.String`
The Id of the element which contains the template.

#### Example
    <%= Html.Kendo().ListView<Order>()
        .Name("Orders")
        .ClientTemplateId("listViewTemplate");
        %>

### 1.Pageable
Allows paging of the data.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Ajax(ajax => ajax.Action("Orders", "ListView"))
        .Pageable();
        %>

### 1.Pageable(System.Action{Kendo.Mvc.UI.Fluent.PageableBuilder})
Allows paging of the data.

#### Parameters

##### pagerAction `System.Action{Kendo.Mvc.UI.Fluent.PageableBuilder}`
Use builder to define paging settings.

#### Parameters

##### pagerAction `System.Action{Kendo.Mvc.UI.Fluent.PageableBuilder}`
Use builder to define paging settings.

#### Example
    <%= Html.Kendo().ListView()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("Orders", "ListView"))
        .Pageable(paging => paging.Enabled(true))
        %>

### 1.Navigatable
Enables keyboard navigation.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Ajax(ajax => ajax.Action("Orders", "ListView"))
        .Navigatable();
        %>

### 1.Selectable
Enables single item selection.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Selectable()
        %>

### 1.Selectable(System.Action{Kendo.Mvc.UI.Fluent.ListViewSelectionSettingsBuilder})
Enables item selection.

#### Parameters

##### selectionAction `System.Action{Kendo.Mvc.UI.Fluent.ListViewSelectionSettingsBuilder}`
Use builder to define the selection mode.

#### Parameters

##### selectionAction `System.Action{Kendo.Mvc.UI.Fluent.ListViewSelectionSettingsBuilder}`
Use builder to define the selection mode.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Selectable(selection => {
        selection.Enabled(true);
        selection.Mode(ListViewSelectionMode.Multiple);
        })
        %>

### 1.TagName(System.String)
Specifies ListView wrapper element tag name.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .TagName("div")
        %>

### 1.Editable(System.Action{Kendo.Mvc.UI.Fluent.ListViewEditingSettingsBuilder{`0}})
Configures the ListView editing settings.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Editable(settings => settings.Enabled(true))
        %>

### 1.Editable
Enables ListView editing.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Editable()
        %>

### 1.Events(System.Action{Kendo.Mvc.UI.Fluent.ListViewEventBuilder})
Configures the client-side events.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ListViewEventBuilder}`
The client events action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ListViewEventBuilder}`
The client events action.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Events(events => events
        .DataBound("onDataBound")
        )
        %>