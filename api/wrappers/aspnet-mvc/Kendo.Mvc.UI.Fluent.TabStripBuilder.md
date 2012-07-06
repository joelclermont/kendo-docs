---
title:Kendo.Mvc.UI.Fluent.TabStripBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.tabstripbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TabStripBuilder

## Methods

### Items(System.Action{Kendo.Mvc.UI.Fluent.TabStripItemFactory})
Defines the items in the tabstrip

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.TabStripItemFactory}`
The add action.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.TabStripItemFactory}`
The add action.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

### Events(System.Action{Kendo.Mvc.UI.Fluent.TabStripEventBuilder})
Configures the client-side events.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.TabStripEventBuilder}`
The client events action.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.TabStripEventBuilder}`
The client events action.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Events(events =>
        events.Select("onSelect").OnLoad("onLoad")
        )
        %>

### Animation(System.Boolean)
Configures the animation effects of the tabstrip.

#### Parameters

##### enable `System.Boolean`
Whether the component animation is enabled.

#### Parameters

##### enable `System.Boolean`
Whether the component animation is enabled.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("PanelBar")
        .Animation(false)

### Animation(System.Action{Kendo.Mvc.UI.Fluent.PopupAnimationBuilder})
Configures the animation effects of the tabstrip.

#### Parameters

##### animationAction `System.Action{Kendo.Mvc.UI.Fluent.PopupAnimationBuilder}`
The action that configures the animation.

#### Parameters

##### animationAction `System.Action{Kendo.Mvc.UI.Fluent.PopupAnimationBuilder}`
The action that configures the animation.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("PanelBar")
        .Animation(animation => animation.Open(config => config.Fade(FadeDirection.In)))

### BindTo(System.String,System.Action{Kendo.Mvc.UI.TabStripItem,Kendo.Mvc.SiteMapNode})
Binds the tabstrip to a sitemap

#### Parameters

##### viewDataKey `System.String`
The view data key.

##### siteMapAction `System.Action{Kendo.Mvc.UI.TabStripItem`
The action to configure the item.

#### Parameters

##### viewDataKey `System.String`
The view data key.

##### siteMapAction `System.Action{Kendo.Mvc.UI.TabStripItem`
The action to configure the item.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .BindTo("examples", (item, siteMapNode) =>
        {
        })
        %>

### BindTo(System.String)
Binds the tabstrip to a sitemap.

#### Parameters

##### viewDataKey `System.String`
The view data key.

#### Parameters

##### viewDataKey `System.String`
The view data key.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .BindTo("examples")
        %>

### BindTo``1(System.Collections.Generic.IEnumerable{``0},System.Action{Kendo.Mvc.UI.TabStripItem,``0})
Binds the tabstrip to a list of objects

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{``0}`
The data source.

##### itemDataBound `System.Action{Kendo.Mvc.UI.TabStripItem`
The action executed for every data bound item.

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{``0}`
The data source.

##### itemDataBound `System.Action{Kendo.Mvc.UI.TabStripItem`
The action executed for every data bound item.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .BindTo(new []{"First", "Second"}, (item, value)
        {
        item.Text = value;
        })
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
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        .SelectedIndex(1)
        %>

### ItemAction(System.Action{Kendo.Mvc.UI.TabStripItem})
Callback for each item.

#### Parameters

##### action `System.Action{Kendo.Mvc.UI.TabStripItem}`
Action, which will be executed for each item.

#### Parameters

##### action `System.Action{Kendo.Mvc.UI.TabStripItem}`
Action, which will be executed for each item.

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

### HighlightPath(System.Boolean)
Select item depending on the current URL.

#### Parameters

##### value `System.Boolean`
If true the item will be highlighted.

#### Parameters

##### value `System.Boolean`
If true the item will be highlighted.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .HighlightPath(true)
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
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .SecurityTrimming(false)
        %>