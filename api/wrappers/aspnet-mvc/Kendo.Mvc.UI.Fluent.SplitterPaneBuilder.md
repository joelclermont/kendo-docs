---
title:Kendo.Mvc.UI.Fluent.SplitterPaneBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.splitterpanebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SplitterPaneBuilder

## Methods

### Size(System.String)
Sets the pane size.

#### Parameters

##### value `System.String`
The desired size. Only sizes in pixels and percentages are allowed.

#### Parameters

##### value `System.String`
The desired size. Only sizes in pixels and percentages are allowed.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Size("220px");
        })
        %>

### MinSize(System.String)
Sets the minimum pane size.

#### Parameters

##### value `System.String`
The desired minimum size. Only sizes in pixels and percentages are allowed.

#### Parameters

##### value `System.String`
The desired minimum size. Only sizes in pixels and percentages are allowed.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().MinSize("220px");
        })
        %>

### MaxSize(System.String)
Sets the maximum pane size.

#### Parameters

##### value `System.String`
The desired maximum size. Only sizes in pixels and percentages are allowed.

#### Parameters

##### value `System.String`
The desired maximum size. Only sizes in pixels and percentages are allowed.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().MaxSize("220px");
        })
        %>

### Scrollable(System.Boolean)
Sets whether the pane shows a scrollbar when its content overflows.

#### Parameters

##### isScrollable `System.Boolean`
Whether the pane will be scrollable.

#### Parameters

##### isScrollable `System.Boolean`
Whether the pane will be scrollable.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Scrollable(false);
        })
        %>

### Resizable(System.Boolean)
Sets whether the pane can be resized by the user.

#### Parameters

##### isResizable `System.Boolean`
Whether the pane will be resizable.

#### Parameters

##### isResizable `System.Boolean`
Whether the pane will be resizable.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Resizable(true);
        })
        %>

### Collapsed(System.Boolean)
Sets whether the pane is initially collapsed.

#### Parameters

##### isCollapsed `System.Boolean`
Whether the pane will be initially collapsed.

#### Parameters

##### isCollapsed `System.Boolean`
Whether the pane will be initially collapsed.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Collapsed(true);
        })
        %>

### Collapsible(System.Boolean)
Sets whether the pane can be collapsed by the user.

#### Parameters

##### isCollapsible `System.Boolean`
Whether the pane can be collapsed by the user.

#### Parameters

##### isCollapsible `System.Boolean`
Whether the pane can be collapsed by the user.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().Collapsible(true);
        })
        %>

### HtmlAttributes(System.Object)
Sets the HTML attributes applied to the outer HTML element rendered for the item

#### Parameters

##### attributes `System.Object`
The attributes.

#### Parameters

##### attributes `System.Object`
The attributes.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes =>
        {
        panes.Add().HtmlAttributes(new { style = "background: red" });
        })
        %>

### HtmlAttributes(System.Collections.Generic.IDictionary{System.String,System.Object})
Sets the HTML attributes applied to the outer HTML element rendered for the item

#### Parameters

##### attributes `System.Collections.Generic.IDictionary{System.String`
The attributes.

#### Parameters

##### attributes `System.Collections.Generic.IDictionary{System.String`
The attributes.

### Content(System.Action)
Sets the HTML content of the pane.

#### Parameters

##### value `System.Action`
The action which renders the HTML content.

#### Parameters

##### value `System.Action`
The action which renders the HTML content.

### Content(System.Func{System.Object,System.Object})
Sets the HTML content of the pane.

#### Parameters

##### value `System.Func{System.Object`
The Razor template for the HTML content.

#### Parameters

##### value `System.Func{System.Object`
The Razor template for the HTML content.

### Content(System.String)
Sets the HTML content of the pane.

#### Parameters

##### value `System.String`
The HTML content.

#### Parameters

##### value `System.String`
The HTML content.

### LoadContentFrom(System.Web.Routing.RouteValueDictionary)
Sets the Url which will be requested to return the pane content.

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the Action method.

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the Action method.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add()
        .LoadContentFrom(MVC.Home.Index().GetRouteValueDictionary());
        })
        %>

### LoadContentFrom(System.String,System.String)
Sets the Url, which will be requested to return the pane content.

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add()
        .LoadContentFrom("AjaxView_OpenSource", "Splitter");
        })
        %>

### LoadContentFrom(System.String,System.String,System.Object)
Sets the Url, which will be requested to return the content.

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

##### routeValues `System.Object`
Route values.

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

##### routeValues `System.Object`
Route values.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add()
        .LoadContentFrom("AjaxView_OpenSource", "Splitter", new { id = 10 });
        })
        %>

### LoadContentFrom(System.String)
Sets the Url, which will be requested to return the pane content.

#### Parameters

##### value `System.String`
The url.

#### Parameters

##### value `System.String`
The url.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add()
        .LoadContentFrom(Url.Action("AjaxView_OpenSource", "Splitter"));
        })
        %>