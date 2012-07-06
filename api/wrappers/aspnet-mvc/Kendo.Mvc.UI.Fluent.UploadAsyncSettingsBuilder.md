---
title:Kendo.Mvc.UI.Fluent.UploadAsyncSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadasyncsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadAsyncSettingsBuilder

## Methods

### AutoUpload(System.Boolean)
Sets a value indicating whether to start the upload immediately after selecting a file

#### Parameters

##### value `System.Boolean`
true if the upload should start immediately after selecting a file, false otherwise; true by default

### Save(System.String,System.String,System.Web.Routing.RouteValueDictionary)
Sets the action, controller and route values for the save operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Save", "Home", new RouteValueDictionary{ {"id", 1} });
        )
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values.

### Save(System.String,System.String,System.Object)
Sets the action, controller and route values for the save operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Save", "Home", new { id = 1 });
        )
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

##### routeValues `System.Object`
The route values.

### Save(System.String,System.String)
Sets the action and controller for the save operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Save", "Home");
        )
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

### Save(System.String)
Sets the route name for the save operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Default");
        )
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

### Save(System.Web.Routing.RouteValueDictionary)
Sets the route values for the save operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save(MVC.Home.Save(1).GetRouteValueDictionary());
        )
        %>

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the action method.

### Save(System.String,System.Web.Routing.RouteValueDictionary)
Sets the route and values for the save operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Default", "Home", new RouteValueDictionary{ {"id", 1} });
        )
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values.

### Save(System.String,System.Object)
Sets the route and values for the save operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Default", new { id = 1 });
        )
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

##### routeValues `System.Object`
The route values.

### Save``1(System.Linq.Expressions.Expression{System.Action{``0}})
Sets the action for the save operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save<HomeController>(controller => controller.Save()));
        )
        %>

#### Parameters

##### controllerAction `System.Linq.Expressions.Expression{System.Action{``0}}`
The action.

### SaveField(System.String)
Sets the field name for the save operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .SaveField("attachment");
        )
        %>

#### Parameters

##### fieldName `System.String`

            The form field name to use for submiting the files.
            The Upload name is used if not set.
            

### SaveUrl(System.String)
Sets an absolute or relative Save action URL.
            Note that the URL must be in the same domain for the upload to succeed.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .SaveUrl("/save");
        )
        %>

#### Parameters

##### url `System.String`
The Save action URL.

### Remove(System.String,System.String,System.Web.Routing.RouteValueDictionary)
Sets the action, controller and route values for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Remove("Remove", "Home", new RouteValueDictionary{ {"id", 1} });
        )
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values.

### Remove(System.String,System.String,System.Object)
Sets the action, controller and route values for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Remove("Remove", "Home", new { id = 1 });
        )
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

##### routeValues `System.Object`
The route values.

### Remove(System.String,System.String)
Sets the action and controller for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Remove("Remove", "Home");
        )
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

### Remove(System.String)
Sets the route name for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Remove("Default");
        )
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

### Remove(System.Web.Routing.RouteValueDictionary)
Sets the route values for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Remove(MVC.Home.Remove(1).GetRouteValueDictionary());
        )
        %>

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the action method.

### Remove(System.String,System.Web.Routing.RouteValueDictionary)
Sets the route and values for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Remove("Default", "Home", new RouteValueDictionary{ {"id", 1} });
        )
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values.

### Remove(System.String,System.Object)
Sets the route and values for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Remove("Default", new { id = 1 });
        )
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

##### routeValues `System.Object`
The route values.

### Remove``1(System.Linq.Expressions.Expression{System.Action{``0}})
Sets the action for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Remove<HomeController>(controller => controller.Remove()));
        )
        %>

#### Parameters

##### controllerAction `System.Linq.Expressions.Expression{System.Action{``0}}`
The action.

### RemoveUrl(System.String)
Sets an absolute or relative Remove action URL.
            Note that the URL must be in the same domain for the operation to succeed.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .RemoveUrl("/remove");
        )
        %>

#### Parameters

##### url `System.String`
The Remove action URL.

### RemoveField(System.String)
Sets the field name for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .RemoveField("attachments");
        )
        %>

#### Parameters

##### fieldName `System.String`

            The form field name to use for submiting the files.
            "fileNames" is used if not set.
            