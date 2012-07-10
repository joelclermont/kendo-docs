---
title:GridColumnFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.gridcolumnfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.GridColumnFactory

Creates columns for the !:Grid{TModel}.

## Methods

### Bound`(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Defines a bound column.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`

### Bound(System.String)
Defines a bound column.

### Bound(System.Type,System.String)
Defines a bound column.

### ForeignKey`(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Collections.IEnumerable,System.String,System.String)
Defines a foreign key column.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
The member which matches the selected item

##### data ```0}}`
The foreign data

##### dataFieldValue `System.Collections.IEnumerable`
The data value field

##### dataFieldText `System.String`
The data text field

### ForeignKey`(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Web.Mvc.SelectList)
Defines a foreign key column.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
The member which matches the selected item

##### data ```0}}`
The foreign data

### AutoGenerate(System.Boolean)
Determines if columns should be automatically generated.

#### Parameters

##### shouldGenerate `System.Boolean`
If true columns should be generated, otherwise false.

### AutoGenerate(System.Action{Kendo.Mvc.UI.GridColumnBase{}})
Determines if columns should be automatically generated.

#### Parameters

##### columnAction `System.Action{Kendo.Mvc.UI.GridColumnBase{}}`
Action which will be executed for each generated column.

### Template(System.Action{})
Defines a template column.

#### Parameters

##### templateAction `System.Action{}`

### Command(System.Action{Kendo.Mvc.UI.Fluent.GridActionCommandFactory{}})
Defines a command column.

#### Parameters

##### commandAction `System.Action{Kendo.Mvc.UI.Fluent.GridActionCommandFactory{}}`