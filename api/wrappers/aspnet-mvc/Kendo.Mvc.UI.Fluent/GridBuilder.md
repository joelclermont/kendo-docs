---
title:Kendo.Mvc.UI.Fluent.GridBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridBuilder

Defines the fluent interface for configuring the  component.

## Methods

### RowTemplate(System.Action{`0,Kendo.Mvc.UI.Grid{`0}})
Sets the row template of the grid

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

#### Parameters

##### codeBlockTemplate `System.Action{`0`
The template

### RowTemplate(System.Action{`0})
Sets the row template of the grid

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

#### Parameters

##### codeBlockTemplate `System.Action{`0}`
The template

### RowTemplate(System.Func{`0,System.Object})
Sets the row template of the grid using Razor syntax

#### Example
    <%= Html.Kendo().Grid(Model)
        .RowTemplate(@<text>
        @item.Name
        @item.Age
        </text>)
        %>

#### Parameters

##### inlineTemplate `System.Func{`0`
The template

### Resizable(System.Action{Kendo.Mvc.UI.Fluent.GridResizingSettingsBuilder})
Configures the grid resizing settings

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Resizable(resizing => resizing.Columns(true))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridResizingSettingsBuilder}`
Resizing settings configurator method

### Reorderable(System.Action{Kendo.Mvc.UI.Fluent.GridReorderingSettingsBuilder})
Configures the grid reordering settings

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Reorderable(reordering => reordering.Columns(true))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridReorderingSettingsBuilder}`
Resizing settings configurator method

### Editable(System.Action{Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder{`0}})
Configures the grid editing settings.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .Editable(settings => settings.Enabled(true))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridEditingSettingsBuilder{`0}}`
Configurator for the edit settings.

### ToolBar(System.Action{Kendo.Mvc.UI.Fluent.GridToolBarCommandFactory{`0}})
Configures the toolbar of the grid.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Orders")
        .ToolBar(commands => commands.Create())
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridToolBarCommandFactory{`0}}`
ToolBar configurator.

### Footer(System.Boolean)
Configure when to show footer of the grid.

#### Parameters

##### visible `System.Boolean`
If it is true, the feature is visible.

### BindTo(System.Collections.Generic.IEnumerable{`0})
Binds the grid to a list of objects

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

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{`0}`
The data source.

### RowAction(System.Action{Kendo.Mvc.UI.GridRow{`0}})
Callback for each row.

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

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.GridRow{`0}}`
Action, which will be executed for each row.
            You can format the entire row

### CellAction(System.Action{Kendo.Mvc.UI.GridCell{`0}})
Callback for each cell.

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

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.GridCell{`0}}`
Action, which will be executed for each cell.
            You can format a concrete cell.

### EnableCustomBinding(System.Boolean)
Enables or disables the custom binding of the grid.

#### Parameters

##### value `System.Boolean`
If true enables custom binding.

### Columns(System.Action{Kendo.Mvc.UI.Fluent.GridColumnFactory{`0}})
Defines the columns of the grid.

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

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridColumnFactory{`0}}`
The add action.

### Sortable
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

### Sortable(System.Action{Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder{`0}})
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
        .Sortable(sorting => sorting.SortMode(GridSortMode.MultipleColumn)
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridSortSettingsBuilder{`0}}`
Use builder to define sort settings.

### Selectable
Enables row selection.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Selectable()
        %>

### Selectable(System.Action{Kendo.Mvc.UI.Fluent.GridSelectionSettingsBuilder})
Enables row selection.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Selectable(selection => selection.Enabled(true))
        %>

#### Parameters

##### selectionAction `System.Action{Kendo.Mvc.UI.Fluent.GridSelectionSettingsBuilder}`
Use builder to define the selection settings.

### PrefixUrlParameters(System.Boolean)
Put grid name as a prefix.

### Pageable
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

### Pageable(System.Action{Kendo.Mvc.UI.Fluent.PageableBuilder})
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
        .Pageable(paging =>
        paging.PageSize(20)
        .Style(GridPagerStyles.NextPreviousAndNumeric)
        .Position(GridPagerPosition.Bottom)
        )
        %>

#### Parameters

##### pagerAction `System.Action{Kendo.Mvc.UI.Fluent.PageableBuilder}`
Use builder to define paging settings.

### Filterable
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

### Filterable(System.Action{Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder})
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
        .Filterable(filtering => filtering.Enabled(true);
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridFilterableSettingsBuilder}`
Use builder to define filtering settings.

### Scrollable
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

### Scrollable(System.Action{Kendo.Mvc.UI.Fluent.GridScrollSettingsBuilder})
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
        .Scrollable(scrolling => scrolling.Enabled(true);
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridScrollSettingsBuilder}`
Use builder to define scrolling settings.

### Navigatable
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

### Navigatable(System.Action{Kendo.Mvc.UI.Fluent.GridNavigatableSettingsBuilder})
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
        .Navigatable(navigation => navigation.Enabled(true));
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridNavigatableSettingsBuilder}`
Use builder to define keyboard navigation settings.

### Events(System.Action{Kendo.Mvc.UI.Fluent.GridEventBuilder})
Enables column context menu.

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

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.GridEventBuilder}`
The client events action.

### Groupable(System.Action{Kendo.Mvc.UI.Fluent.GridGroupingSettingsBuilder})
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

### Groupable
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