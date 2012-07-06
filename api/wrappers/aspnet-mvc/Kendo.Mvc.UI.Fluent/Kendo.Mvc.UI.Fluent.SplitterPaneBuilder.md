---
title:Kendo.Mvc.UI.Fluent.SplitterPaneBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.splitterpanebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SplitterPaneBuilder

## Methods

### Size(System.String)
Sets the pane size.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Size("220px");
        })
        %>

#### Parameters

##### value `System.String`
The desired size. Only sizes in pixels and percentages are allowed.

### MinSize(System.String)
Sets the minimum pane size.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().MinSize("220px");
        })
        %>

#### Parameters

##### value `System.String`
The desired minimum size. Only sizes in pixels and percentages are allowed.

### MaxSize(System.String)
Sets the maximum pane size.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().MaxSize("220px");
        })
        %>

#### Parameters

##### value `System.String`
The desired maximum size. Only sizes in pixels and percentages are allowed.

### Scrollable(System.Boolean)
Sets whether the pane shows a scrollbar when its content overflows.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Scrollable(false);
        })
        %>

#### Parameters

##### isScrollable `System.Boolean`
Whether the pane will be scrollable.

### Resizable(System.Boolean)
Sets whether the pane can be resized by the user.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Resizable(true);
        })
        %>

#### Parameters

##### isResizable `System.Boolean`
Whether the pane will be resizable.

### Collapsed(System.Boolean)
Sets whether the pane is initially collapsed.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Collapsed(true);
        })
        %>

#### Parameters

##### isCollapsed `System.Boolean`
Whether the pane will be initially collapsed.

### Collapsible(System.Boolean)
Sets whether the pane can be collapsed by the user.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Collapsible(true);
        })
        %>

#### Parameters

##### isCollapsible `System.Boolean`
Whether the pane can be collapsed by the user.

### HtmlAttributes(System.Object)
Sets the HTML attributes applied to the outer HTML element rendered for the item

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().HtmlAttributes(new { style = "background: red" });
        })
        %>

#### Parameters

##### attributes `System.Object`
The attributes.

### HtmlAttributes(System.Collections.Generic.IDictionary{System.String,System.Object})
Sets the HTML attributes applied to the outer HTML element rendered for the item

#### Parameters

##### attributes `System.Collections.Generic.IDictionary{System.String`
The attributes.

### Content(System.Action)
Sets the HTML content of the pane.

#### Parameters

##### value `System.Action`
The action which renders the HTML content.

### Content(System.Func{System.Object,System.Object})
Sets the HTML content of the pane.

#### Parameters

##### value `System.Func{System.Object`
The Razor template for the HTML content.

### Content(System.String)
Sets the HTML content of the pane.

#### Parameters

##### value `System.String`
The HTML content.

### LoadContentFrom(System.Web.Routing.RouteValueDictionary)
Sets the Url which will be requested to return the pane content.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add()
        .LoadContentFrom(MVC.Home.Index().GetRouteValueDictionary());
        })
        %>

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the Action method.

### LoadContentFrom(System.String,System.String)
Sets the Url, which will be requested to return the pane content.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add()
        .LoadContentFrom("AjaxView_OpenSource", "Splitter");
        })
        %>

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

### LoadContentFrom(System.String,System.String,System.Object)
Sets the Url, which will be requested to return the content.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add()
        .LoadContentFrom("AjaxView_OpenSource", "Splitter", new { id = 10 });
        })
        %>

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

##### routeValues `System.Object`
Route values.

### LoadContentFrom(System.String)
Sets the Url, which will be requested to return the pane content.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add()
        .LoadContentFrom(Url.Action("AjaxView_OpenSource", "Splitter"));
        })
        %>

#### Parameters

##### value `System.String`
The url.