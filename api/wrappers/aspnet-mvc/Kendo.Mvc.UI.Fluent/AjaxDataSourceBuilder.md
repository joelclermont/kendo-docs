---
title:AjaxDataSourceBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.ajaxdatasourcebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.AjaxDataSourceBuilder

Defines the fluent interface for configuring the DataSource AJAX create/update/destroy operation bindings.

## Methods

### Update(System.Action\<Kendo.Mvc.UI.Fluent.CrudOperationBuilder\>)
Configures the URL for Update operation.

### Update(System.String,System.String)
Sets controller and action for Update operation.

#### Parameters

##### actionName `System.String`
Action name

##### controllerName `System.String`
Controller Name

### Update(System.String,System.String,System.Object)
Sets controller, action and routeValues for Update operation.

#### Parameters

##### actionName `System.String`
Action name

##### controllerName `System.String`
Controller Name

##### routeValues `System.Object`
Route values

### Create(System.Action\<Kendo.Mvc.UI.Fluent.CrudOperationBuilder\>)
Configures the URL for Create operation.

### Create(System.String,System.String)
Sets controller and action for Create operation.

#### Parameters

##### actionName `System.String`
Action name

##### controllerName `System.String`
Controller Name

### Create(System.String,System.String,System.Object)
Sets controller, action and routeValues for Create operation.

#### Parameters

##### actionName `System.String`
Action name

##### controllerName `System.String`
Controller Name

##### routeValues `System.Object`
Route values

### Destroy(System.Action\<Kendo.Mvc.UI.Fluent.CrudOperationBuilder\>)
Configures the URL for Destroy operation.

### Destroy(System.String,System.String)
Sets controller and action for Destroy operation.

#### Parameters

##### actionName `System.String`
Action name

##### controllerName `System.String`
Controller Name

### Destroy(System.String,System.String,System.Object)
Sets controller, action and routeValues for Destroy operation.

#### Parameters

##### actionName `System.String`
Action name

##### controllerName `System.String`
Controller Name

##### routeValues `System.Object`
Route values

### Model(System.Action\<Kendo.Mvc.UI.Fluent.DataSourceModelDescriptorFactory\<T\>\>)
Configures Model properties

### Batch(System.Boolean)
Determines if modifications will be sent to the server in batches or as individually requests.

#### Parameters

##### enabled `System.Boolean`
If true changes will be batched, otherwise false.