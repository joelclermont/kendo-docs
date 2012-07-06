---
title:Kendo.Mvc.UI.Fluent.GridColumnFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.gridcolumnfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.GridColumnFactory

## Methods

### 1.Bound``1(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Defines a bound column.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`

            

### 1.Bound(System.String)
Defines a bound column.

### 1.Bound(System.Type,System.String)
Defines a bound column.

### 1.ForeignKey``1(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Collections.IEnumerable,System.String,System.String)
Defines a foreign key column.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`

            

### 1.ForeignKey``1(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Web.Mvc.SelectList)
Defines a foreign key column.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`

            

### 1.AutoGenerate(System.Boolean)
Determines if columns should be automatically generated.

#### Parameters

##### shouldGenerate `System.Boolean`
If true columns should be generated, otherwise false.

### 1.AutoGenerate(System.Action{Kendo.Mvc.UI.GridColumnBase{`0}})
Determines if columns should be automatically generated.

#### Parameters

##### columnAction `System.Action{Kendo.Mvc.UI.GridColumnBase{`0}}`
Action which will be executed for each generated column.

### 1.Template(System.Action{`0})
Defines a template column.

#### Parameters

##### templateAction `System.Action{`0}`

            

### 1.Command(System.Action{Kendo.Mvc.UI.Fluent.GridActionCommandFactory{`0}})
Defines a command column.

#### Parameters

##### commandAction `System.Action{Kendo.Mvc.UI.Fluent.GridActionCommandFactory{`0}}`

            