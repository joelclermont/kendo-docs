---
title:FilterDescriptor
slug:aspnetmvc-kendo.mvc.filterdescriptor
publish:true
---

# Kendo.Mvc.FilterDescriptor

Represents declarative filtering.

## Properties

### Member
Gets or sets the member name which will be used for filtering.

### MemberType
Gets or sets the type of the member that is used for filtering.
            Set this property if the member type cannot be resolved automatically.
            Such cases are: items with ICustomTypeDescriptor, XmlNode or DataRow.
            Changing this property did not raise

### Operator
Gets or sets the filter operator.

### Value
Gets or sets the target filter value.

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