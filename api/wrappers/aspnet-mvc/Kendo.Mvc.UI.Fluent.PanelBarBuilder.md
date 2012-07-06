---
title:Kendo.Mvc.UI.Fluent.PanelBarBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.panelbarbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PanelBarBuilder

## Methods

### Items(System.Action{Kendo.Mvc.UI.Fluent.PanelBarItemFactory})
Defines the items in the panelbar

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.PanelBarItemFactory}`
The add action.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.PanelBarItemFactory}`
The add action.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

### Events(System.Action{Kendo.Mvc.UI.Fluent.PanelBarEventBuilder})
Configures the client-side events.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.PanelBarEventBuilder}`
The client events action.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.PanelBarEventBuilder}`
The client events action.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Events(events =>
        events.Expand("expand").Collapse("collapse")
        )
        %>

### BindTo(System.String,System.Action{Kendo.Mvc.UI.PanelBarItem,Kendo.Mvc.SiteMapNode})
Binds the panelbar to a sitemap

#### Parameters

##### viewDataKey `System.String`
The view data key.

##### siteMapAction `System.Action{Kendo.Mvc.UI.PanelBarItem`
The action to configure the item.

#### Parameters

##### viewDataKey `System.String`
The view data key.

##### siteMapAction `System.Action{Kendo.Mvc.UI.PanelBarItem`
The action to configure the item.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .BindTo("examples", (item, siteMapNode) =>
        {
        })
        %>

### BindTo(System.String)
Binds the panelbar to a sitemap.

#### Parameters

##### viewDataKey `System.String`
The view data key.

#### Parameters

##### viewDataKey `System.String`
The view data key.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .BindTo("examples")
        %>

### BindTo``1(System.Collections.Generic.IEnumerable{``0},System.Action{Kendo.Mvc.UI.PanelBarItem,``0})
Binds the panelbar to a list of objects

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{``0}`
The data source.

##### itemDataBound `System.Action{Kendo.Mvc.UI.PanelBarItem`
The action executed for every data bound item.

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{``0}`
The data source.

##### itemDataBound `System.Action{Kendo.Mvc.UI.PanelBarItem`
The action executed for every data bound item.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .BindTo(new []{"First", "Second"}, (item, value)
        {
        item.Text = value;
        })
        %>

### BindTo(System.Collections.IEnumerable,System.Action{Kendo.Mvc.UI.NavigationBindingFactory{Kendo.Mvc.UI.PanelBarItem}})
Binds the panelbar to a list of objects. The panelbar will create a hierarchy of items using the specified mappings.

#### Parameters

##### dataSource `System.Collections.IEnumerable`
The data source.

##### factoryAction `System.Action{Kendo.Mvc.UI.NavigationBindingFactory{Kendo.Mvc.UI.PanelBarItem}}`
The action which will configure the mappings

#### Parameters

##### dataSource `System.Collections.IEnumerable`
The data source.

##### factoryAction `System.Action{Kendo.Mvc.UI.NavigationBindingFactory{Kendo.Mvc.UI.PanelBarItem}}`
The action which will configure the mappings

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

### Animation(System.Boolean)
Configures the animation effects of the panelbar.

#### Parameters

##### enable `System.Boolean`
Whether the component animation is enabled.

#### Parameters

##### enable `System.Boolean`
Whether the component animation is enabled.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Animation(false)

### Animation(System.Action{Kendo.Mvc.UI.Fluent.ExpandableAnimationBuilder})
Configures the animation effects of the panelbar.

#### Parameters

##### animationAction `System.Action{Kendo.Mvc.UI.Fluent.ExpandableAnimationBuilder}`
The action that configures the animation.

#### Parameters

##### animationAction `System.Action{Kendo.Mvc.UI.Fluent.ExpandableAnimationBuilder}`
The action that configures the animation.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Animation(animation => animation.Expand(config => config.Fade(FadeDirection.In)))

### ItemAction(System.Action{Kendo.Mvc.UI.PanelBarItem})
Callback for each item.

#### Parameters

##### itemAction `System.Action{Kendo.Mvc.UI.PanelBarItem}`
Action, which will be executed for each item.

#### Parameters

##### itemAction `System.Action{Kendo.Mvc.UI.PanelBarItem}`
Action, which will be executed for each item.

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

### HighlightPath(System.Boolean)
Select item depending on the current URL.

#### Parameters

##### value `System.Boolean`
If true the item will be highlighted.

#### Parameters

##### value `System.Boolean`
If true the item will be highlighted.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .HighlightPath(true)
        %>

### ExpandAll(System.Boolean)
Renders the panelbar with expanded items.

#### Parameters

##### value `System.Boolean`
If true the panelbar will be expanded.

#### Parameters

##### value `System.Boolean`
If true the panelbar will be expanded.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .ExpandAll(true)
        %>

### ExpandMode(Kendo.Mvc.UI.PanelBarExpandMode)
Sets the expand mode of the panelbar.

#### Parameters

##### value `Kendo.Mvc.UI.PanelBarExpandMode`
The desired expand mode.

#### Parameters

##### value `Kendo.Mvc.UI.PanelBarExpandMode`
The desired expand mode.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .ExpandMode(PanelBarExpandMode.Multiple)
        %>

### SelectedIndex(System.Int32)
Selects the item at the specified index.

#### Parameters

##### index `System.Int32`
The index.

#### Parameters

##### index `System.Int32`
The index.

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

### SecurityTrimming(System.Boolean)
Enable/disable security trimming functionality of the component.

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .SecurityTrimming(false)
        %>