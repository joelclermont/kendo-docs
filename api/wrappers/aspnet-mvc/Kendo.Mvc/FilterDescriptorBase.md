---
title:Kendo.Mvc.FilterDescriptorBase
slug:aspnetmvc-kendo.mvc.filterdescriptorbase
publish:true
---

# Kendo.Mvc.FilterDescriptorBase

Base class for all IFilterDescriptor used for
            handling the logic for property changed notifications.

## Methods

### CreateFilterExpression(System.Linq.Expressions.Expression)
Creates a filter expression by delegating its creation to
            M:Kendo.Mvc.FilterDescriptorBase.CreateFilterExpression(System.Linq.Expressions.Expression), if
             is ParameterExpression, otherwise throws ArgumentException

#### Parameters

##### instance `System.Linq.Expressions.Expression`
The instance expression, which will be used for filtering.

#### Returns
A predicate filter expression.

### CreateFilterExpression(System.Linq.Expressions.ParameterExpression)
Creates a predicate filter expression used for collection filtering.

#### Parameters

##### parameterExpression `System.Linq.Expressions.ParameterExpression`
The parameter expression, which will be used for filtering.

#### Returns
A predicate filter expression.