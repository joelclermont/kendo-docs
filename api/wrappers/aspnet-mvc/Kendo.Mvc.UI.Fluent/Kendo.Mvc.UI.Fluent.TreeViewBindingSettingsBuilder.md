---
title:Kendo.Mvc.UI.Fluent.TreeViewBindingSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.treeviewbindingsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TreeViewBindingSettingsBuilder

## Methods

### Enabled(System.Boolean)
Enables or disables binding.

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataBinding(dataBinding =>
        {
        dataBinding.Ajax().Select("Index", "Home").Enabled((bool)ViewData["ajax"]);
        })
        %>

### Select(System.Web.Routing.RouteValueDictionary)
Sets the action, controller and route values

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .DataBinding(dataBinding =>
        {
        dataBinding.Ajax().Select(MVC.Home.Index(1).GetRouteValueDictionary());
        })
        %>

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the Action method.

### Select(System.String,System.String,System.Web.Routing.RouteValueDictionary)
Sets the action, controller and route values for the select operation

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataBinding(dataBinding =>
        {
        dataBinding.Ajax().Select("Index", "Home", new RouteValueDictionary{ {"id", 1} });
        })
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values.

### Select(System.String,System.String,System.Object)
Sets the action, controller and route values for the select operation

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataBinding(dataBinding =>
        {
        dataBinding.Ajax().Select("Index", "Home", new { {"id", 1} });
        })
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

##### routeValues `System.Object`
The route values.

### Select(System.String,System.String)
Sets the action, controller and route values for the select operation

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataBinding(dataBinding =>
        {
        dataBinding.Ajax().Select("Index", "Home");
        })
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

### Select(System.String,System.Web.Routing.RouteValueDictionary)
Sets the route and values for the select operation

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataBinding(dataBinding =>
        {
        dataBinding.Ajax().Select("Default", "Home", new RouteValueDictionary{ {"id", 1} });
        })
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values.

### Select(System.String,System.Object)
Sets the route and values for the select operation

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataBinding(dataBinding =>
        {
        dataBinding.Ajax().Select("Default", new {id=1});
        })
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

##### routeValues `System.Object`
The route values.

### Select(System.String)
Sets the route name for the select operation

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .DataBinding(dataBinding =>
        {
        dataBinding.Ajax().Select("Default");
        })
        %>

#### Parameters

##### routeName `System.String`
Name of the route.