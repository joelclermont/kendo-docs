---
title:PanelBarBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.panelbarbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PanelBarBuilder

Defines the fluent interface for configuring the PanelBar component.

## Methods

### Items(System.Action\<Kendo.Mvc.UI.Fluent.PanelBarItemFactory\>)
Defines the items in the panelbar

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

#### Parameters

##### addAction System.Action\<[Kendo.Mvc.UI.Fluent.PanelBarItemFactory](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/PanelBarItemFactory)\>
The add action.

### Events(System.Action\<Kendo.Mvc.UI.Fluent.PanelBarEventBuilder\>)
Configures the client-side events.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events =>
        events.Expand("expand").Collapse("collapse")
        )
        %>

#### Parameters

##### clientEventsAction System.Action\<[Kendo.Mvc.UI.Fluent.PanelBarEventBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/PanelBarEventBuilder)\>
The client events action.

### BindTo(System.String,System.Action\<Kendo.Mvc.UI.PanelBarItem,Kendo.Mvc.SiteMapNode\>)
Binds the panelbar to a sitemap

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .BindTo("examples", (item, siteMapNode) =>
        {
        })
        %>

#### Parameters

##### viewDataKey `System.String`
The view data key.

##### siteMapAction System.Action\<[Kendo.Mvc.UI.PanelBarItem](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/PanelBarItem),Kendo.Mvc.SiteMapNode\>
The action to configure the item.

### BindTo(System.String)
Binds the panelbar to a sitemap.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .BindTo("examples")
        %>

#### Parameters

##### viewDataKey `System.String`
The view data key.

### BindTo\<T1\>(System.Collections.Generic.IEnumerable\<T1\>,System.Action\<Kendo.Mvc.UI.PanelBarItem,T1\>)
Binds the panelbar to a list of objects

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .BindTo(new []{"First", "Second"}, (item, value)
        {
        item.Text = value;
        })
        %>

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable<T1>`
The data source.

##### itemDataBound System.Action\<[Kendo.Mvc.UI.PanelBarItem](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/PanelBarItem),T1\>
The action executed for every data bound item.

### BindTo(System.Collections.IEnumerable,System.Action\<Kendo.Mvc.UI.Fluent.NavigationBindingFactory\<Kendo.Mvc.UI.PanelBarItem\>\>)
Binds the panelbar to a list of objects. The panelbar will create a hierarchy of items using the specified mappings.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .BindTo(Model, mapping => mapping
        .For<Customer>(binding => binding
        .Children(c => c.Orders) // The "child" items will be bound to the the "Orders" property
        .ItemDataBound((item, c) => item.Text = c.ContactName) // Map "Customer" properties to PanelBarItem properties
        )
        .For<Order<(binding => binding
        .Children(o => null) // "Orders" do not have child objects so return "null"
        .ItemDataBound((item, o) => item.Text = o.OrderID.ToString()) // Map "Order" properties to PanelBarItem properties
        )
        )
        %>

#### Parameters

##### dataSource `System.Collections.IEnumerable`
The data source.

##### factoryAction System.Action\<[Kendo.Mvc.UI.Fluent.NavigationBindingFactory](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/NavigationBindingFactory)\<Kendo.Mvc.UI.PanelBarItem\>\>
The action which will configure the mappings

### Animation(System.Boolean)
Configures the animation effects of the panelbar.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Animation(false)

#### Parameters

##### enable `System.Boolean`
Whether the component animation is enabled.

### Animation(System.Action\<Kendo.Mvc.UI.Fluent.ExpandableAnimationBuilder\>)
Configures the animation effects of the panelbar.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Animation(animation => animation.Expand(config => config.Fade(FadeDirection.In)))

#### Parameters

##### animationAction System.Action\<[Kendo.Mvc.UI.Fluent.ExpandableAnimationBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/ExpandableAnimationBuilder)\>
The action that configures the animation.

### ItemAction(System.Action\<Kendo.Mvc.UI.PanelBarItem\>)
Callback for each item.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .ItemAction(item =>
        {
        item
        .Text(...)
        .HtmlAttributes(...);
        })
        %>

#### Parameters

##### itemAction System.Action\<[Kendo.Mvc.UI.PanelBarItem](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/PanelBarItem)\>
Action, which will be executed for each item.

### HighlightPath(System.Boolean)
Select item depending on the current URL.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .HighlightPath(true)
        %>

#### Parameters

##### value `System.Boolean`
If true the item will be highlighted.

### ExpandAll(System.Boolean)
Renders the panelbar with expanded items.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .ExpandAll(true)
        %>

#### Parameters

##### value `System.Boolean`
If true the panelbar will be expanded.

### ExpandMode(Kendo.Mvc.UI.PanelBarExpandMode)
Sets the expand mode of the panelbar.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .ExpandMode(PanelBarExpandMode.Multiple)
        %>

#### Parameters

##### value [Kendo.Mvc.UI.PanelBarExpandMode](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/PanelBarExpandMode)
The desired expand mode.

### SelectedIndex(System.Int32)
Selects the item at the specified index.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        .SelectedIndex(1)
        %>

#### Parameters

##### index `System.Int32`
The index.

### SecurityTrimming(System.Boolean)
Enable/disable security trimming functionality of the component.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .SecurityTrimming(false)
        %>

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.