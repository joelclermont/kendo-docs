---
title:Kendo.Mvc.UI.Fluent.GridColumnFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.gridcolumnfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.GridColumnFactory

Creates columns for the .

## Methods

### Bound``1(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Defines a bound column.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`

### Bound(System.String)
Defines a bound column.

### Bound(System.Type,System.String)
Defines a bound column.

### ForeignKey``1(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Collections.IEnumerable,System.String,System.String)
Defines a foreign key column.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`

### ForeignKey``1(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Web.Mvc.SelectList)
Defines a foreign key column.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`

### AutoGenerate(System.Boolean)
Determines if columns should be automatically generated.

#### Parameters

##### shouldGenerate `System.Boolean`
If true columns should be generated, otherwise false.

### AutoGenerate(System.Action{Kendo.Mvc.UI.GridColumnBase{`0}})
Determines if columns should be automatically generated.

#### Parameters

##### columnAction `System.Action{Kendo.Mvc.UI.GridColumnBase{`0}}`
Action which will be executed for each generated column.

### Template(System.Action{`0})
Defines a template column.

#### Parameters

##### templateAction `System.Action{`0}`

### Command(System.Action{Kendo.Mvc.UI.Fluent.GridActionCommandFactory{`0}})
Defines a command column.

#### Parameters

##### commandAction `System.Action{Kendo.Mvc.UI.Fluent.GridActionCommandFactory{`0}}`