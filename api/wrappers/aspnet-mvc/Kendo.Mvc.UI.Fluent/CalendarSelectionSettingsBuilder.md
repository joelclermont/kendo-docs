---
title:CalendarSelectionSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.calendarselectionsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.CalendarSelectionSettingsBuilder

Defines the fluent interface for configuring the CalendarSelectionSettings.

## Methods

### Dates(System.Collections.Generic.IList{System.DateTime})
Defines list of dates. This list determines which dates to be rendered with action link.

#### Parameters

##### dates `System.Collections.Generic.IList{System.DateTime}`
List of DateTime objects

### Action(System.Web.Routing.RouteValueDictionary)
Sets the action to which the date should navigate

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the Action method.

### Action(System.String,System.String,System.Object)
Sets the action to which the item should navigate

#### Parameters

##### action `System.String`
Name of the action.

##### controller `System.String`
Name of the controller.

##### values `System.Object`
The route values.