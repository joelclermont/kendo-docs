---
title:Kendo.Mvc.UI.Fluent.GridBoundColumnBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridboundcolumnbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridBoundColumnBuilder

## Methods

### 1.Format(System.String)
Gets or sets the format for displaying the data.

#### Parameters

##### value `System.String`
The value.

#### Parameters

##### value `System.String`
The value.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderDate).Format("{0:dd/MM/yyyy}"))
        %>

### 1.EditorViewData(System.Object)
Provides additional view data in the editor template for that column (if any).

#### Parameters

##### additionalViewData `System.Object`
An anonymous object which contains the additional data

#### Parameters

##### additionalViewData `System.Object`
An anonymous object which contains the additional data

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => {
        columns.Bound(o => o.Customer).EditorViewData(new { customers = Model.Customers });
        })
        %>

### 1.EditorTemplateName(System.String)
Specify which editor template should be used for the column

#### Parameters

##### templateName `System.String`
name of the editor template

#### Parameters

##### templateName `System.String`
name of the editor template

### 1.Sortable(System.Boolean)
Enables or disables sorting the column. All bound columns are sortable by default.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderDate).Sortable(false))
        %>

### 1.Groupable(System.Boolean)
Enables or disables grouping by that column. All bound columns are groupable by default.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderDate).Groupable(false))
        %>

### 1.Filterable(System.Boolean)
Enables or disables filtering the column. All bound columns are filterable by default.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderDate).Filterable(false))
        %>

### 1.Encoded(System.Boolean)
Enables or disables HTML encoding the data of the column. All bound columns are encoded by default.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderDate).Encoded(false))
        %>

### 1.Template(System.Action{`0})
Sets the template for the column.

#### Parameters

##### templateAction `System.Action{`0}`
The action defining the template.

#### Parameters

##### templateAction `System.Action{`0}`
The action defining the template.

#### Example
    <% Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns
        .Add(c => c.CustomerID)
        .Template(() =>
        {
        %>
        >img
        alt="<%= c.CustomerID %>"
        src="<%= Url.Content("~/Content/Grid/Customers/" + c.CustomerID + ".jpg") %>"
        />
        <%
        }).Title("Picture");)
        .Render();
        %>

### 1.FooterTemplate(System.Action{Kendo.Mvc.UI.GridAggregateResult})
Sets the footer template for the column.

#### Parameters

##### template `System.Action{Kendo.Mvc.UI.GridAggregateResult}`
The action defining the template.

#### Parameters

##### template `System.Action{Kendo.Mvc.UI.GridAggregateResult}`
The action defining the template.

### 1.FooterTemplate(System.Func{Kendo.Mvc.UI.GridAggregateResult,System.Object})
Sets the footer template for the column.

#### Parameters

##### template `System.Func{Kendo.Mvc.UI.GridAggregateResult`
The action defining the template.

#### Parameters

##### template `System.Func{Kendo.Mvc.UI.GridAggregateResult`
The action defining the template.

### 1.GroupFooterTemplate(System.Action{Kendo.Mvc.UI.GridAggregateResult})
Sets the group footer template for the column.

#### Parameters

##### template `System.Action{Kendo.Mvc.UI.GridAggregateResult}`
The action defining the template.

#### Parameters

##### template `System.Action{Kendo.Mvc.UI.GridAggregateResult}`
The action defining the template.

### 1.GroupFooterTemplate(System.Func{Kendo.Mvc.UI.GridAggregateResult,System.Object})
Sets the group footer template for the column.

#### Parameters

##### template `System.Func{Kendo.Mvc.UI.GridAggregateResult`
The action defining the template.

#### Parameters

##### template `System.Func{Kendo.Mvc.UI.GridAggregateResult`
The action defining the template.

### 1.GroupHeaderTemplate(System.Action{Kendo.Mvc.UI.GridGroupAggregateResult})
Sets the group footer template for the column.

#### Parameters

##### template `System.Action{Kendo.Mvc.UI.GridGroupAggregateResult}`
The action defining the template.

#### Parameters

##### template `System.Action{Kendo.Mvc.UI.GridGroupAggregateResult}`
The action defining the template.

### 1.GroupHeaderTemplate(System.Func{Kendo.Mvc.UI.GridGroupAggregateResult,System.Object})
Sets the group footer template for the column.

#### Parameters

##### template `System.Func{Kendo.Mvc.UI.GridGroupAggregateResult`
The action defining the template.

#### Parameters

##### template `System.Func{Kendo.Mvc.UI.GridGroupAggregateResult`
The action defining the template.