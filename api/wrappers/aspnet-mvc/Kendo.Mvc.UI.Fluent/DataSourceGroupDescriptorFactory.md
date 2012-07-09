---
title:Kendo.Mvc.UI.Fluent.DataSourceGroupDescriptorFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.datasourcegroupdescriptorfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.DataSourceGroupDescriptorFactory

Defines the fluent interface for configuring group.

## Methods

### Add`(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Specifies the member by which the data should be grouped.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
Member access expression which describes the member

### Add`(System.String)
Specifies the member by which the data should be grouped.

#### Parameters

##### memberName `System.String`
Member name

### Add(System.String,System.Type)
Specifies the member by which the data should be grouped.

#### Parameters

##### memberName `System.String`
Member name

##### memberType `System.Type`
Member type

### Add(System.String,System.Type,System.ComponentModel.ListSortDirection)
Specifies the member by which the data should be grouped.

#### Parameters

##### memberName `System.String`
Member name

##### memberType `System.Type`
Member type

##### sortDirection `System.ComponentModel.ListSortDirection`
Sort order

### Add`(System.String,System.ComponentModel.ListSortDirection)
Specifies the member by which the data should be grouped.

#### Parameters

##### memberName `System.String`
Member type

##### sortDirection `System.ComponentModel.ListSortDirection`
Sort order

### AddDescending`(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Specifies the member by which the data should be sorted in descending order and grouped.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
Member access expression which describes the member

### AddDescending`(System.String)
Specifies the member by which the data should be sorted in descending order and grouped.

#### Parameters

##### memberName `System.String`
Member name

### AddDescending(System.String,System.Type)
Specifies the member by which the data should be sorted in descending order and grouped.

#### Parameters

##### memberName `System.String`
Member name

##### memberType `System.Type`
Member type