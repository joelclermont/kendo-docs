---
title:MenuBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.menubuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.MenuBuilder

Defines the fluent interface for configuring the Menu component.

## Methods

### Items(System.Action\<Kendo.Mvc.UI.Fluent.MenuItemFactory\>)
Defines the items in the menu

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

#### Parameters

##### addAction System.Action\<[Kendo.Mvc.UI.Fluent.MenuItemFactory](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/MenuItemFactory)\>
The add action.

### Events(System.Action\<Kendo.Mvc.UI.Fluent.MenuEventBuilder\>)
Configures the client-side events.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Events(events =>
        events.Open("onOpen").OnClose("onClose")
        )
        %>

#### Parameters

##### clientEventsAction System.Action\<[Kendo.Mvc.UI.Fluent.MenuEventBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/MenuEventBuilder)\>
The client events action.

### Orientation(Kendo.Mvc.UI.MenuOrientation)
Sets the menu orientation.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Orientation(MenuOrientation.Vertical)
        %>

#### Parameters

##### value [Kendo.Mvc.UI.MenuOrientation](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/MenuOrientation)
The desired orientation.

### OpenOnClick(System.Boolean)
Enables or disables the "open-on-click" feature.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .OpenOnClick(true)
        %>

### CloseOnClick(System.Boolean)
Specifies that sub menus should close after item selection (provided they won't navigate).

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .CloseOnClick(false)
        %>

### HoverDelay(System.Int32)
Specifies the delay in ms before the menu is opened/closed - used to avoid accidental closure on leaving.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .HoverDelay(300)
        %>

### BindTo(System.String,System.Action\<Kendo.Mvc.UI.MenuItem,Kendo.Mvc.SiteMapNode\>)
Binds the menu to a sitemap

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .BindTo("examples", (item, siteMapNode) =>
        {
        })
        %>

#### Parameters

##### viewDataKey `System.String`
The view data key.

##### siteMapAction System.Action\<[Kendo.Mvc.UI.MenuItem](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/MenuItem),Kendo.Mvc.SiteMapNode\>
The action to configure the item.

### BindTo(System.String)
Binds the menu to a sitemap.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .BindTo("examples")
        %>

#### Parameters

##### viewDataKey `System.String`
The view data key.

### BindTo\<T1\>(System.Collections.Generic.IEnumerable\<T1\>,System.Action\<Kendo.Mvc.UI.MenuItem,T1\>)
Binds the menu to a list of objects. The menu will be "flat" which means a menu item will be created for
            every item in the data source.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .BindTo(new []{"First", "Second"}, (item, value)
        {
        item.Text = value;
        })
        %>

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable<T1>`
The data source.

##### itemDataBound System.Action\<[Kendo.Mvc.UI.MenuItem](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/MenuItem),T1\>
The action executed for every data bound item.

### BindTo(System.Collections.IEnumerable,System.Action\<Kendo.Mvc.UI.Fluent.NavigationBindingFactory\<Kendo.Mvc.UI.MenuItem\>\>)
Binds the menu to a list of objects. The menu will create a hierarchy of items using the specified mappings.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .BindTo(Model, mapping => mapping
        .For<Customer>(binding => binding
        .Children(c => c.Orders) // The "child" items will be bound to the the "Orders" property
        .ItemDataBound((item, c) => item.Text = c.ContactName) // Map "Customer" properties to MenuItem properties
        )
        .For<Order<(binding => binding
        .Children(o => null) // "Orders" do not have child objects so return "null"
        .ItemDataBound((item, o) => item.Text = o.OrderID.ToString()) // Map "Order" properties to MenuItem properties
        )
        )
        %>

#### Parameters

##### dataSource `System.Collections.IEnumerable`
The data source.

##### factoryAction System.Action\<[Kendo.Mvc.UI.Fluent.NavigationBindingFactory](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/NavigationBindingFactory)\<Kendo.Mvc.UI.MenuItem\>\>
The action which will configure the mappings

### ItemAction(System.Action\<Kendo.Mvc.UI.MenuItem\>)
Callback for each item.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .ItemAction(item =>
        {
        item
        .Text(...)
        .HtmlAttributes(...);
        })
        %>

#### Parameters

##### action System.Action\<[Kendo.Mvc.UI.MenuItem](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/MenuItem)\>
Action, which will be executed for each item.

### HighlightPath(System.Boolean)
Select item depending on the current URL.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .HighlightPath(true)
        %>

#### Parameters

##### value `System.Boolean`
If true the item will be highlighted.

### SecurityTrimming(System.Boolean)
Enable/disable security trimming functionality of the component.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .SecurityTrimming(false)
        %>

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.