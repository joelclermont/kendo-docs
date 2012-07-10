---
title:DataSourceModelDescriptorFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.datasourcemodeldescriptorfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.DataSourceModelDescriptorFactory

Defines the fluent interface for configuring the DataSource Model definition.

## Methods

### Id`(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Specify the member used to identify an unique Model instance.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
Member access expression which describes the member

### Id(System.String)
Specify the member used to identify an unique Model instance.

#### Parameters

##### fieldName `System.String`
The member name.

### Field`(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Describes a Model field

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
Member access expression which describes the field

### Field(System.String,System.Type)
Describes a Model field

#### Parameters

##### memberName `System.String`
Field name

##### memberType `System.Type`
Field type

### Field`(System.String)
Describes a Model field

#### Parameters

##### memberName `System.String`
Member name