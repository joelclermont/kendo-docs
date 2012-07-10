---
title:GroupDescriptor
slug:aspnetmvc-kendo.mvc.groupdescriptor
publish:true
---

# Kendo.Mvc.GroupDescriptor

Represents grouping criteria.

## Properties

### MemberType
Gets or sets the type of the member that is used for grouping.
            Set this property if the member type cannot be resolved automatically.
            Such cases are: items with ICustomTypeDescriptor, XmlNode or DataRow.
            Changing this property did not raise
            PropertyChanged event.

### DisplayContent
Gets or sets the content which will be used from UI.

### AggregateFunctions
Gets or sets the aggregate functions used when grouping is executed.

## Methods

### CycleSortDirection
Changes the SortDescriptor to the next logical value.