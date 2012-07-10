---
title:QueryableExtensions
slug:aspnetmvc-kendo.mvc.extensions.queryableextensions
publish:true
---

# Kendo.Mvc.Extensions.QueryableExtensions

Provides extension methods to process DataSourceRequest.

## Methods

### Sort(System.Linq.IQueryable,System.Collections.Generic.IEnumerable{Kendo.Mvc.SortDescriptor})
Sorts the elements of a sequence using the specified sort descriptors.

#### Parameters

##### source `System.Linq.IQueryable`
A sequence of values to sort.

##### sortDescriptors `System.Collections.Generic.IEnumerable{Kendo.Mvc.SortDescriptor}`
The sort descriptors used for sorting.

#### Returns
An IQueryable whose elements are sorted according to a .

### Page(System.Linq.IQueryable,System.Int32,System.Int32)
Pages through the elements of a sequence until the specified
             using .

#### Parameters

##### source `System.Linq.IQueryable`
A sequence of values to page.

##### pageIndex `System.Int32`
Index of the page.

##### pageSize `System.Int32`
Size of the page.

#### Returns
An IQueryable whose elements are at the specified .

### Select(System.Linq.IQueryable,System.Linq.Expressions.LambdaExpression)
Projects each element of a sequence into a new form.

#### Parameters

##### source `System.Linq.IQueryable`
A sequence of values to project.

##### selector `System.Linq.Expressions.LambdaExpression`
A projection function to apply to each element.

#### Returns
An IQueryable whose elements are the result of invoking a
            projection selector on each element of .

### GroupBy(System.Linq.IQueryable,System.Linq.Expressions.LambdaExpression)
Groups the elements of a sequence according to a specified key selector function.

#### Parameters

##### source `System.Linq.IQueryable`
An IQueryable whose elements to group.

##### keySelector `System.Linq.Expressions.LambdaExpression`
A function to extract the key for each element.

#### Returns
An IQueryable with !:IGrouping{TKey,TElement} items,
            whose elements contains a sequence of objects and a key.

### OrderBy(System.Linq.IQueryable,System.Linq.Expressions.LambdaExpression)
Sorts the elements of a sequence in ascending order according to a key.

#### Parameters

##### source `System.Linq.IQueryable`
A sequence of values to order.

##### keySelector `System.Linq.Expressions.LambdaExpression`
A function to extract a key from an element.

#### Returns
An IQueryable whose elements are sorted according to a key.

### OrderByDescending(System.Linq.IQueryable,System.Linq.Expressions.LambdaExpression)
Sorts the elements of a sequence in descending order according to a key.

#### Parameters

##### source `System.Linq.IQueryable`
A sequence of values to order.

##### keySelector `System.Linq.Expressions.LambdaExpression`
A function to extract a key from an element.

#### Returns
An IQueryable whose elements are sorted in descending order according to a key.

### OrderBy(System.Linq.IQueryable,System.Linq.Expressions.LambdaExpression,System.Nullable{System.ComponentModel.ListSortDirection})
Calls M:Kendo.Mvc.Extensions.QueryableExtensions.OrderBy(System.Linq.IQueryable,System.Linq.Expressions.LambdaExpression)
            or M:Kendo.Mvc.Extensions.QueryableExtensions.OrderByDescending(System.Linq.IQueryable,System.Linq.Expressions.LambdaExpression) depending on the .

#### Parameters

##### source `System.Linq.IQueryable`
The source.

##### keySelector `System.Linq.Expressions.LambdaExpression`
The key selector.

##### sortDirection `System.Nullable{System.ComponentModel.ListSortDirection}`
The sort direction.

#### Returns
An IQueryable whose elements are sorted according to a key.

### GroupBy(System.Linq.IQueryable,System.Collections.Generic.IEnumerable{Kendo.Mvc.GroupDescriptor})
Groups the elements of a sequence according to a specified .

#### Parameters

##### source `System.Linq.IQueryable`
An IQueryable whose elements to group.

##### groupDescriptors `System.Collections.Generic.IEnumerable{Kendo.Mvc.GroupDescriptor}`
The group descriptors used for grouping.

#### Returns
An IQueryable with IGroup items,
            whose elements contains a sequence of objects and a key.

### Aggregate(System.Linq.IQueryable,System.Collections.Generic.IEnumerable{Kendo.Mvc.AggregateFunction})
Calculates the results of given aggregates functions on a sequence of elements.

#### Parameters

##### source `System.Linq.IQueryable`
An IQueryable whose elements will
            be used for aggregate calculation.

##### aggregateFunctions `System.Collections.Generic.IEnumerable{Kendo.Mvc.AggregateFunction}`
The aggregate functions.

#### Returns
Collection of AggregateResults calculated for each function.

### Where(System.Linq.IQueryable,System.Linq.Expressions.Expression)
Filters a sequence of values based on a predicate.

#### Parameters

##### source `System.Linq.IQueryable`
An IQueryable to filter.

##### predicate `System.Linq.Expressions.Expression`
A function to test each element for a condition.

#### Returns
An IQueryable that contains elements from the input sequence
            that satisfy the condition specified by .

### Where(System.Linq.IQueryable,System.Collections.Generic.IEnumerable{Kendo.Mvc.IFilterDescriptor})
Filters a sequence of values based on a collection of IFilterDescriptor.

#### Parameters

##### source `System.Linq.IQueryable`
The source.

##### filterDescriptors `System.Collections.Generic.IEnumerable{Kendo.Mvc.IFilterDescriptor}`
The filter descriptors.

#### Returns
An IQueryable that contains elements from the input sequence
            that satisfy the conditions specified by each filter descriptor in .

### Take(System.Linq.IQueryable,System.Int32)
Returns a specified number of contiguous elements from the start of a sequence.

#### Parameters

##### source `System.Linq.IQueryable`
The sequence to return elements from.

##### count `System.Int32`
The number of elements to return.

#### Returns
An IQueryable that contains the specified number
            of elements from the start of .

### Skip(System.Linq.IQueryable,System.Int32)
Bypasses a specified number of elements in a sequence
            and then returns the remaining elements.

#### Parameters

##### source `System.Linq.IQueryable`
An IQueryable to return elements from.

##### count `System.Int32`
The number of elements to skip before returning the remaining elements.

#### Returns
An IQueryable that contains elements that occur
            after the specified index in the input sequence.

### Count(System.Linq.IQueryable)
Returns the number of elements in a sequence.

#### Parameters

##### source `System.Linq.IQueryable`
The IQueryable that contains the elements to be counted.

#### Returns
The number of elements in the input sequence.

### ElementAt(System.Linq.IQueryable,System.Int32)
Returns the element at a specified index in a sequence.

#### Parameters

##### source `System.Linq.IQueryable`
An IQueryable to return an element from.

##### index `System.Int32`
The zero-based index of the element to retrieve.

#### Returns
The element at the specified position in .