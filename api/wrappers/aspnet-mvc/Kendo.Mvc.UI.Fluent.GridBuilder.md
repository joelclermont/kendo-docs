---
title:Kendo.Mvc.UI.Fluent.GridBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridBuilder

## Methods

### 1.RowTemplate(System.Action{`0,Kendo.Mvc.UI.Grid{`0}})
Sets the row template of the grid

#### Parameters

##### codeBlockTemplate `System.Action{`0`
The template

#### Parameters

##### codeBlockTemplate `System.Action{`0`
The template

#### Example
    <%= Html.Kendo().Grid(Model)
        .RowTemplate(o =>
        {
        %>
        <%= o.Name %>
        <%= o.Age %>
        <%
        })
        %>

### 1.RowTemplate(System.Action{`0})
Sets the row template of the grid

#### Parameters

##### codeBlockTemplate `System.Action{`0}`
The template

#### Parameters

##### codeBlockTemplate `System.Action{`0}`
The template

#### Example
    <%= Html.Kendo().Grid(Model)
        .RowTemplate(o =>
        {
        %>
        <%= o.Name %>
        <%= o.Age %>
        <%
        })
        %>

### 1.RowTemplate(System.Func{`0,System.Object})
Sets the row template of the grid using Razor syntax

#### Parameters

##### inlineTemplate `System.Func{`0`
The template

#### Parameters

##### inlineTemplate `System.Func{`0`
The template

#### Example
    <%= Html.Kendo().Grid(Model)
        .RowTemplate(@<text>
        @item.Name
        @item.Age
        </text>)
        %>

### 1.Resizable(System.Action{Kendo.Mvc.UI.Fluent.GridResizingSettingsBuilder})
Configures the grid resizing settings

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridResizingSettingsBuilder}`
Resizing settings configurator method

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridResizingSettingsBuilder}`
Resizing settings configurator method

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Resizable(resizing => resizing.Columns(true))
        %>

### 1.Reorderable(System.Action{Kendo.Mvc.UI.Fluent.GridReorderingSettingsBuilder})
Configures the grid reordering settings

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridReorderingSettingsBuilder}`
Resizing settings configurator method

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridReorderingSettingsBuilder}`
Resizing settings configurator method

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Reorderable(reordering => reordering.Columns(true))
        %>

### 1.Editable(System.Action{Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder{`0}})
Configures the grid editing settings.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder{`0}}`
Configurator for the edit settings.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder{`0}}`
Configurator for the edit settings.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Editable(settings => settings.Enabled(true))
        %>

### 1.ToolBar(System.Action{Kendo.Mvc.UI.Fluent.GridToolBarCommandFactory{`0}})
Configures the toolbar of the grid.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridToolBarCommandFactory{`0}}`
ToolBar configurator.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridToolBarCommandFactory{`0}}`
ToolBar configurator.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .ToolBar(commands => commands.Create())
        %>

### 1.Footer(System.Boolean)
Configure when to show footer of the grid.

#### Parameters

##### visible `System.Boolean`
If it is true, the feature is visible.

#### Parameters

##### visible `System.Boolean`
If it is true, the feature is visible.

### 1.BindTo(System.Collections.Generic.IEnumerable{`0})
Binds the grid to a list of objects

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{`0}`
The data source.

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{`0}`
The data source.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"]);
        %>

### 1.RowAction(System.Action{Kendo.Mvc.UI.GridRow{`0}})
Callback for each row.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.GridRow{`0}}`
Action, which will be executed for each row.
            You can format the entire row

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.GridRow{`0}}`
Action, which will be executed for each row.
            You can format the entire row

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .RowAction(row =>
        {
        // "DataItem" is the Order object to which the current row is bound to
        if (row.DataItem.Freight > 10)
        {
        //Set the background of the entire row
        row.HtmlAttributes["style"] = "background:red;";
        }
        });
        %>

### 1.CellAction(System.Action{Kendo.Mvc.UI.GridCell{`0}})
Callback for each cell.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.GridCell{`0}}`
Action, which will be executed for each cell.
            You can format a concrete cell.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.GridCell{`0}}`
Action, which will be executed for each cell.
            You can format a concrete cell.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .CellAction(cell =>
        {
        if (cell.Column.Name == "Freight")
        {
        if (cell.DataItem.Freight > 10)
        {
        //Set the background of this cell only
        cell.HtmlAttributes["style"] = "background:red;";
        }
        }
        });
        %>

### 1.EnableCustomBinding(System.Boolean)
Enables or disables the custom binding of the grid.

#### Parameters

##### value `System.Boolean`
If true enables custom binding.

#### Parameters

##### value `System.Boolean`
If true enables custom binding.

### 1.Columns(System.Action{Kendo.Mvc.UI.Fluent.GridColumnFactory{`0}})
Defines the columns of the grid.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridColumnFactory{`0}}`
The add action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridColumnFactory{`0}}`
The add action.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"]);
        %>

### 1.Sortable
Allows sorting of the columns.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Sortable();
        %>

### 1.Sortable(System.Action{Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder{`0}})
Allows sorting of the columns.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder{`0}}`
Use builder to define sort settings.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder{`0}}`
Use builder to define sort settings.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Sortable(sorting => sorting.SortMode(GridSortMode.MultipleColumn)
        %>

### 1.Selectable
Enables row selection.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Selectable()
        %>

### 1.Selectable(System.Action{Kendo.Mvc.UI.Fluent.GridSelectionSettingsBuilder})
Enables row selection.

#### Parameters

##### selectionAction `System.Action{Kendo.Mvc.UI.Fluent.GridSelectionSettingsBuilder}`
Use builder to define the selection settings.

#### Parameters

##### selectionAction `System.Action{Kendo.Mvc.UI.Fluent.GridSelectionSettingsBuilder}`
Use builder to define the selection settings.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Selectable(selection => selection.Enabled(true))
        %>

### 1.PrefixUrlParameters(System.Boolean)
Put grid name as a prefix.

### 1.Pageable
Allows paging of the data.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
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
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Pageable(paging =>
        paging.PageSize(20)
        .Style(GridPagerStyles.NextPreviousAndNumeric)
        .Position(GridPagerPosition.Bottom)
        )
        %>

### 1.Filterable
Allows filtering of the columns.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Filterable();
        %>

### 1.Filterable(System.Action{Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder})
Allows filtering of the columns.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder}`
Use builder to define filtering settings.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder}`
Use builder to define filtering settings.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Filterable(filtering => filtering.Enabled(true);
        %>

### 1.Scrollable
Show scrollbar if there are many items.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Scrollable();
        %>

### 1.Scrollable(System.Action{Kendo.Mvc.UI.Fluent.GridScrollSettingsBuilder})
Show scrollbar if there are many items.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridScrollSettingsBuilder}`
Use builder to define scrolling settings.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridScrollSettingsBuilder}`
Use builder to define scrolling settings.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Scrollable(scrolling => scrolling.Enabled(true);
        %>

### 1.Navigatable
Enables keyboard navigation.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Navigatable();
        %>

### 1.Navigatable(System.Action{Kendo.Mvc.UI.Fluent.GridNavigatableSettingsBuilder})
Enables keyboard navigation.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridNavigatableSettingsBuilder}`
Use builder to define keyboard navigation settings.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridNavigatableSettingsBuilder}`
Use builder to define keyboard navigation settings.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Navigatable(navigation => navigation.Enabled(true));
        %>

### 1.Events(System.Action{Kendo.Mvc.UI.Fluent.GridEventBuilder})
Enables column context menu.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridEventBuilder}`
The client events action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridEventBuilder}`
The client events action.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .ColumnContextMenu();
        %>
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events
        .DataBinding("onDataBinding")
        )
        %>

### 1.Groupable(System.Action{Kendo.Mvc.UI.Fluent.GridGroupingSettingsBuilder})
Use it to configure grouping.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Groupable(grouping => grouping.Enabled(true);
        %>

### 1.Groupable
Allows grouping.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Groupable();
        %>