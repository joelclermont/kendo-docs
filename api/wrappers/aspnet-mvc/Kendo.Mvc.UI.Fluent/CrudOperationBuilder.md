---
title:CrudOperationBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.crudoperationbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.CrudOperationBuilder

Defines the fluent interface for configuring the CrudOperation options.

## Methods

### Route(System.Web.Routing.RouteValueDictionary)
Sets the route values for the operation.

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
Route values

### Action(System.String,System.String,System.Object)
Sets the action, contoller and route values for the operation.

#### Parameters

##### actionName `System.String`
Action name

##### controllerName `System.String`
Controller name

##### routeValues `System.Object`
Route values

### Action(System.String,System.String,System.Web.Routing.RouteValueDictionary)
Sets the action, contoller and route values for the operation.

#### Parameters

##### actionName `System.String`
Action name

##### controllerName `System.String`
Controller name

##### routeValues `System.Web.Routing.RouteValueDictionary`
Route values

### Action(System.String,System.String)
Sets the action and contoller values for the operation.

#### Parameters

##### actionName `System.String`
Action name

##### controllerName `System.String`
Controller name

### Route(System.String,System.Web.Routing.RouteValueDictionary)
Sets the route name and values for the operation.

#### Parameters

##### routeName `System.String`
Route name

##### routeValues `System.Web.Routing.RouteValueDictionary`
Route values

### Route(System.String,System.Object)
Sets the route name and values for the operation.

#### Parameters

##### routeName `System.String`
Route name

##### routeValues `System.Object`
Route values

### Route(System.String)
Sets the route name for the operation.

#### Parameters

##### routeName `System.String`

### Data(System.Func\<System.Object,System.Object\>)
Sets JavaScript function which to return additional parameters which to be sent the server.

### Data(System.String)
Sets JavaScript function which to return additional parameters which to be sent the server.

#### Parameters

##### handler `System.String`
JavaScript function name

### Url(System.String)
Specifies an absolute or relative URL for the operation.

#### Parameters

##### url `System.String`
Absolute or relative URL for the operation

### Type(System.Web.Mvc.HttpVerbs)
Specifies the HTTP verb of the request.

#### Parameters

##### verb `System.Web.Mvc.HttpVerbs`
The HTTP verb