---
title:DataSourceModelDescriptorFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.datasourcemodeldescriptorfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.DataSourceModelDescriptorFactory

Defines the fluent interface for configuring the DataSource Model definition.

## Methods

### Id<T1>(System.Linq.Expressions.Expression<System.Func<T,T1>>)
Specify the member used to identify an unique Model instance.

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
Member access expression which describes the member

### Id(System.String)
Specify the member used to identify an unique Model instance.

#### Parameters

##### fieldName `System.String`
The member name.

### Field<T1>(System.Linq.Expressions.Expression<System.Func<T,T1>>)
Describes a Model field

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
Member access expression which describes the field

### Field(System.String,System.Type)
Describes a Model field

#### Parameters

##### memberName `System.String`
Field name

##### memberType `System.Type`
Field type

### Field<T1>(System.String)
Describes a Model field

#### Parameters

##### memberName `System.String`
Member name