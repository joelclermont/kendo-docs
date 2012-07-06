---
title:Kendo.Mvc.UI.Fluent.GridColumnBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.gridcolumnbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.GridColumnBuilderBase

## Methods

### 2.Title(System.String)
Sets the title displayed in the header of the column.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderID).Title("ID"))
        %>

#### Parameters

##### text `System.String`
The text.

### 2.HeaderHtmlAttributes(System.Object)
Sets the HTML attributes applied to the header cell of the column.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderID).HeaderHtmlAttributes(new {@class="order-header"}))
        %>

#### Parameters

##### attributes `System.Object`
The attributes.

### 2.HeaderHtmlAttributes(System.Collections.Generic.IDictionary{System.String,System.Object})
Sets the HTML attributes applied to the header cell of the column.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderID).HeaderHtmlAttributes(new {@class="order-header"}))
        %>

#### Parameters

##### attributes `System.Collections.Generic.IDictionary{System.String`
The attributes.

### 2.FooterHtmlAttributes(System.Object)
Sets the HTML attributes applied to the footer cell of the column.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderID).FooterHtmlAttributes(new {@class="order-footer"}))
        %>

#### Parameters

##### attributes `System.Object`
The attributes.

### 2.FooterHtmlAttributes(System.Collections.Generic.IDictionary{System.String,System.Object})
Sets the HTML attributes applied to the footer cell of the column.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderID).FooterHtmlAttributes(new {@class="order-footer"}))
        %>

#### Parameters

##### attributes `System.Collections.Generic.IDictionary{System.String`
The attributes.

### 2.HtmlAttributes(System.Object)
Sets the HTML attributes applied to the content cell of the column.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderID).HtmlAttributes(new {@class="order-cell"}))
        %>

#### Parameters

##### attributes `System.Object`
The attributes.

### 2.HtmlAttributes(System.Collections.Generic.IDictionary{System.String,System.Object})
Sets the HTML attributes applied to the content cell of the column.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderID).HtmlAttributes(new {@class="order-cell"}))
        %>

#### Parameters

##### attributes `System.Collections.Generic.IDictionary{System.String`
The attributes.

### 2.Width(System.Int32)
Sets the width of the column in pixels.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderID).Width(100))
        %>

#### Parameters

##### pixelWidth `System.Int32`
The width in pixels.

### 2.Width(System.String)
Sets the width of the column using CSS syntax.

#### Example
    <% Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o =>
        {
        %>
        <%= Html.ActionLink("Edit", "Home", new { id = o.OrderID}) %>
        <%
        })
        .Width("30px")
        .Render();
        %>

#### Parameters

##### value `System.String`
The width to set.

### 2.Visible(System.Boolean)
Makes the column visible or not. By default all columns are visible. Invisible columns are not rendered in the output HTML.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Columns(columns => columns.Bound(o => o.OrderID).Visible((bool)ViewData["visible"]))
        %>

### 2.HeaderTemplate(System.Action)
Sets the header template for the column.

#### Parameters

##### template `System.Action`
The action defining the template.

### 2.HeaderTemplate(System.String)
Sets the header template for the column.

#### Parameters

##### template `System.String`
The string defining the template.

### 2.HeaderTemplate(System.Func{System.Object,System.Object})
Sets the header template for the column.

#### Parameters

##### template `System.Func{System.Object`
The action defining the template.

### 2.FooterTemplate(System.Action)
Sets the footer template for the column.

#### Parameters

##### template `System.Action`
The action defining the template.

### 2.FooterTemplate(System.String)
Sets the footer template for the column.

#### Parameters

##### template `System.String`
The string defining the template.

### 2.FooterTemplate(System.Func{System.Object,System.Object})
Sets the footer template for the column.

#### Parameters

##### template `System.Func{System.Object`
The action defining the template.