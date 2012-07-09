---
title:Kendo.Mvc.FilterDescriptor
slug:aspnetmvc-kendo.mvc.filterdescriptor
publish:true
---

# Kendo.Mvc.FilterDescriptor

Represents declarative filtering.

## Methods

### CreateFilterExpression(System.Linq.Expressions.ParameterExpression)
Creates a predicate filter expression.

#### Parameters

##### parameterExpression `System.Linq.Expressions.ParameterExpression`
The parameter expression, which will be used for filtering.

#### Returns
A predicate filter expression.

### Equals(Kendo.Mvc.FilterDescriptor)
Determines whether the specified  descriptor
            is equal to the current one.

#### Parameters

##### other `Kendo.Mvc.FilterDescriptor`
The other filter descriptor.

#### Returns
True if all members of the current descriptor are
            equal to the ones of , otherwise false.

### Equals(System.Object)
Determines whether the specified 
            is equal to the current descriptor.

### GetHashCode
Serves as a hash function for a particular type.

#### Returns
A hash code for the current filter descriptor.