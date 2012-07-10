---
title:GridColumnFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.gridcolumnfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.GridColumnFactory

Creates columns for the !:Grid{TModel}.

## Methods

### Bound\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>)
Defines a bound column.

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T,T1>>`

### Bound(System.String)
Defines a bound column.

### Bound(System.Type,System.String)
Defines a bound column.

### ForeignKey\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Collections.IEnumerable,System.String,System.String)
Defines a foreign key column.

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
The member which matches the selected item

##### data `System.Collections.IEnumerable`
The foreign data

##### dataFieldValue `System.String`
The data value field

##### dataFieldText `System.String`
The data text field

### ForeignKey\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Web.Mvc.SelectList)
Defines a foreign key column.

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
The member which matches the selected item

##### data `System.Web.Mvc.SelectList`
The foreign data

### AutoGenerate(System.Boolean)
Determines if columns should be automatically generated.

#### Parameters

##### shouldGenerate `System.Boolean`
If true columns should be generated, otherwise false.

### AutoGenerate(System.Action\<Kendo.Mvc.UI.GridColumnBase\<T\>\>)
Determines if columns should be automatically generated.

#### Parameters

##### columnAction `System.Action<Kendo.Mvc.UI.GridColumnBase<T>>`
Action which will be executed for each generated column.

### Template(System.Action\<T\>)
Defines a template column.

#### Parameters

##### templateAction `System.Action<T>`

### Command(System.Action\<Kendo.Mvc.UI.Fluent.GridActionCommandFactory\<T\>\>)
Defines a command column.

#### Parameters

##### commandAction `System.Action<Kendo.Mvc.UI.Fluent.GridActionCommandFactory<T>>`