---
title:TabStripBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.tabstripbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TabStripBuilder

Defines the fluent interface for configuring the TabStrip component.

## Methods

### Items(System.Action<Kendo.Mvc.UI.Fluent.TabStripItemFactory>)
Defines the items in the tabstrip

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

#### Parameters

##### addAction System.Action<[Kendo.Mvc.UI.Fluent.TabStripItemFactory>](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/TabStripItemFactory>)>
The add action.

### Events(System.Action<Kendo.Mvc.UI.Fluent.TabStripEventBuilder>)
Configures the client-side events.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events =>
        events.Select("onSelect").OnLoad("onLoad")
        )
        %>

#### Parameters

##### clientEventsAction System.Action<[Kendo.Mvc.UI.Fluent.TabStripEventBuilder>](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/TabStripEventBuilder>)>
The client events action.

### Animation(System.Boolean)
Configures the animation effects of the tabstrip.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("PanelBar")
        .Animation(false)

#### Parameters

##### enable `System.Boolean`
Whether the component animation is enabled.

### Animation(System.Action<Kendo.Mvc.UI.Fluent.PopupAnimationBuilder>)
Configures the animation effects of the tabstrip.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("PanelBar")
        .Animation(animation => animation.Open(config => config.Fade(FadeDirection.In)))

#### Parameters

##### animationAction System.Action<[Kendo.Mvc.UI.Fluent.PopupAnimationBuilder>](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/PopupAnimationBuilder>)>
The action that configures the animation.

### BindTo(System.String,System.Action<Kendo.Mvc.UI.TabStripItem,Kendo.Mvc.SiteMapNode>)
Binds the tabstrip to a sitemap

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .BindTo("examples", (item, siteMapNode) =>
        {
        })
        %>

#### Parameters

##### viewDataKey `System.String`
The view data key.

##### siteMapAction System.Action<[Kendo.Mvc.UI.TabStripItem](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/TabStripItem)
The action to configure the item.

### BindTo(System.String)
Binds the tabstrip to a sitemap.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .BindTo("examples")
        %>

#### Parameters

##### viewDataKey `System.String`
The view data key.

### BindTo<T1>(System.Collections.Generic.IEnumerable<T1>,System.Action<Kendo.Mvc.UI.TabStripItem,<T1>)
Binds the tabstrip to a list of objects

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .BindTo(new []{"First", "Second"}, (item, value)
        {
        item.Text = value;
        })
        %>

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable<T1>`
The data source.

##### itemDataBound System.Action<[Kendo.Mvc.UI.TabStripItem](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/TabStripItem)
The action executed for every data bound item.

### SelectedIndex(System.Int32)
Selects the item at the specified index.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
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

### ItemAction(System.Action<Kendo.Mvc.UI.TabStripItem>)
Callback for each item.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .ItemAction(item =>
        {
        item
        .Text(...)
        .HtmlAttributes(...);
        })
        %>

#### Parameters

##### action System.Action<[Kendo.Mvc.UI.TabStripItem>](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/TabStripItem>)>
Action, which will be executed for each item.

### HighlightPath(System.Boolean)
Select item depending on the current URL.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .HighlightPath(true)
        %>

#### Parameters

##### value `System.Boolean`
If true the item will be highlighted.

### SecurityTrimming(System.Boolean)
Enable/disable security trimming functionality of the component.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .SecurityTrimming(false)
        %>

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.