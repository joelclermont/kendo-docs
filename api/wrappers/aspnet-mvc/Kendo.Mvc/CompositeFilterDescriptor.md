---
title:Kendo.Mvc.CompositeFilterDescriptor
slug:aspnetmvc-kendo.mvc.compositefilterdescriptor
publish:true
---

# Kendo.Mvc.CompositeFilterDescriptor

Represents a filtering descriptor which serves as a container for one or more child filtering descriptors.

## Methods

### CreateFilterExpression(System.Linq.Expressions.ParameterExpression)
Creates a predicate filter expression combining FilterDescriptors
            expressions with LogicalOperator.

#### Parameters

##### parameterExpression `System.Linq.Expressions.ParameterExpression`
The parameter expression, which will be used for filtering.

#### Returns
A predicate filter expression.