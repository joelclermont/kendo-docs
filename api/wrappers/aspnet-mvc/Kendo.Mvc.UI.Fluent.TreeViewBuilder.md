---
title:Kendo.Mvc.UI.Fluent.TreeViewBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treeviewbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewBuilder

## Methods

### Items(System.Action{Kendo.Mvc.UI.Fluent.TreeViewItemFactory})
Defines the items in the TreeView

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.TreeViewItemFactory}`
The add action.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.TreeViewItemFactory}`
The add action.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

### Events(System.Action{Kendo.Mvc.UI.Fluent.TreeViewEventBuilder})
Configures the client-side events.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.TreeViewEventBuilder}`
The client events action.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.TreeViewEventBuilder}`
The client events action.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Events(events =>
        .OnDataBinding("onDataBinding")
        .OnItemDataBound("onItemDataBound")
        )
        %>

### BindTo(System.String,System.Action{Kendo.Mvc.UI.TreeViewItem,Kendo.Mvc.SiteMapNode})
Binds the TreeView to a sitemap

#### Parameters

##### viewDataKey `System.String`
The view data key.

##### siteMapAction `System.Action{Kendo.Mvc.UI.TreeViewItem`
The action to configure the item.

#### Parameters

##### viewDataKey `System.String`
The view data key.

##### siteMapAction `System.Action{Kendo.Mvc.UI.TreeViewItem`
The action to configure the item.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .BindTo("examples", (item, siteMapNode) =>
        {
        })
        %>

### BindTo(System.String)
Binds the TreeView to a sitemap.

#### Parameters

##### viewDataKey `System.String`
The view data key.

#### Parameters

##### viewDataKey `System.String`
The view data key.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .BindTo("examples")
        %>

### BindTo(System.Collections.Generic.IEnumerable{Kendo.Mvc.UI.TreeViewItemModel})
Binds the TreeView to a list of items.
            Use if a hierarchy of items is being sent from the controller; to bind the TreeView declaratively, use the Items() method.

#### Parameters

##### items `System.Collections.Generic.IEnumerable{Kendo.Mvc.UI.TreeViewItemModel}`
The list of items

#### Parameters

##### items `System.Collections.Generic.IEnumerable{Kendo.Mvc.UI.TreeViewItemModel}`
The list of items

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .BindTo(model)
        %>

### BindTo``1(System.Collections.Generic.IEnumerable{``0},System.Action{Kendo.Mvc.UI.TreeViewItem,``0})
Binds the TreeView to a list of objects. The TreeView will be "flat" which means a TreeView item will be created for
            every item in the data source.

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{``0}`
The data source.

##### itemDataBound `System.Action{Kendo.Mvc.UI.TreeViewItem`
The action executed for every data bound item.

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{``0}`
The data source.

##### itemDataBound `System.Action{Kendo.Mvc.UI.TreeViewItem`
The action executed for every data bound item.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .BindTo(new []{"First", "Second"}, (item, value)
        {
        item.Text = value;
        })
        %>

### BindTo(System.Collections.IEnumerable,System.Action{Kendo.Mvc.UI.NavigationBindingFactory{Kendo.Mvc.UI.TreeViewItem}})
Binds the TreeView to a list of objects. The TreeView will create a hierarchy of items using the specified mappings.

#### Parameters

##### dataSource `System.Collections.IEnumerable`
The data source.

##### factoryAction `System.Action{Kendo.Mvc.UI.NavigationBindingFactory{Kendo.Mvc.UI.TreeViewItem}}`
The action which will configure the mappings

#### Parameters

##### dataSource `System.Collections.IEnumerable`
The data source.

##### factoryAction `System.Action{Kendo.Mvc.UI.NavigationBindingFactory{Kendo.Mvc.UI.TreeViewItem}}`
The action which will configure the mappings

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .BindTo(Model, mapping => mapping
        .For<Customer>(binding => binding
        .Children(c => c.Orders) // The "child" items will be bound to the the "Orders" property
        .ItemDataBound((item, c) => item.Text = c.ContactName) // Map "Customer" properties to TreeViewItem properties
        )
        .For<Order<(binding => binding
        .Children(o => null) // "Orders" do not have child objects so return "null"
        .ItemDataBound((item, o) => item.Text = o.OrderID.ToString()) // Map "Order" properties to TreeViewItem properties
        )
        )
        %>

### ItemAction(System.Action{Kendo.Mvc.UI.TreeViewItem})
Callback for each item.

#### Parameters

##### action `System.Action{Kendo.Mvc.UI.TreeViewItem}`
Action, which will be executed for each item.

#### Parameters

##### action `System.Action{Kendo.Mvc.UI.TreeViewItem}`
Action, which will be executed for each item.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .ItemAction(item =>
        {
        item
        .Text(...)
        .HtmlAttributes(...);
        })
        %>

### HighlightPath(System.Boolean)
Select item depending on the current URL.

#### Parameters

##### value `System.Boolean`
If true the item will be highlighted.

#### Parameters

##### value `System.Boolean`
If true the item will be highlighted.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .HighlightPath(true)
        %>

### ExpandAll(System.Boolean)
Expand all the items.

#### Parameters

##### value `System.Boolean`
If true all the items will be expanded.

#### Parameters

##### value `System.Boolean`
If true all the items will be expanded.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .ExpandAll(true)
        %>

### ShowCheckBox(System.Boolean)
ShowCheckBox indicates if checkbox displayed before node.

#### Parameters

##### value `System.Boolean`
If true checkbox will be displayed for every node.

#### Parameters

##### value `System.Boolean`
If true checkbox will be displayed for every node.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .ShowCheckBox(true)
        %>

### DragAndDrop(System.Boolean)
Enables drag & drop between treeview nodes.

#### Parameters

##### value `System.Boolean`
If true, drag & drop is enabled.

#### Parameters

##### value `System.Boolean`
If true, drag & drop is enabled.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        .DragAndDrop(true)
        %>

### SecurityTrimming(System.Boolean)
Enable/disable security trimming functionality of the component.

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .SecurityTrimming(false)
        %>

### DataTextField(System.String)
Sets the name of the field that will supply the item text.

#### Parameters

##### field `System.String`
The field name.

#### Parameters

##### field `System.String`
The field name.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataTextField("Name")
        %>

### DataUrlField(System.String)
Sets the name of the field that will supply the item URL.

#### Parameters

##### field `System.String`
The field name.

#### Parameters

##### field `System.String`
The field name.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataUrlField("LinksTo")
        %>

### DataSpriteCssClassField(System.String)
Sets the name of the field that will supply the CSS class for the item sprite image.

#### Parameters

##### field `System.String`
The field name.

#### Parameters

##### field `System.String`
The field name.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataSpriteCssClassField("IconSprite")
        %>

### DataImageUrlField(System.String)
Sets the name of the field that will supply the URL for the item image.

#### Parameters

##### field `System.String`
The field name.

#### Parameters

##### field `System.String`
The field name.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataImageUrlField("ImageURL")
        %>

### DataSource(System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyDataSourceBuilder})
Configure the DataSource of the component

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyDataSourceBuilder}`
The action that configures the .

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyDataSourceBuilder}`
The action that configures the .

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataSource(dataSource => dataSource
        .Read(read => read
        .Action("Employees", "TreeView")
        )
        )
        %>