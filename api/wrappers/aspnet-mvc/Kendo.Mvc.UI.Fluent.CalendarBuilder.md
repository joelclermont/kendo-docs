---
title:Kendo.Mvc.UI.Fluent.CalendarBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.calendarbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.CalendarBuilder

## Methods

### Events(System.Action{Kendo.Mvc.UI.Fluent.CalendarEventBuilder})
Configures the client-side events.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.CalendarEventBuilder}`
The client events action.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.CalendarEventBuilder}`
The client events action.

#### Example
    <%= Html.Kendo().Calendar()
        .Name("Calendar")
        .Events(events =>
        events.Select("onSelect")
        )
        %>

### Format(System.String)
Sets the date format, which will be used to parse and format the machine date.

### Min(System.String)
Sets the minimal date, which can be selected in the calendar.

### Max(System.String)
Sets the maximal date, which can be selected in the calendar.

### Min(System.DateTime)
Sets the minimal date, which can be selected in the calendar

### Max(System.DateTime)
Sets the maximal date, which can be selected in the calendar

### Value(System.Nullable{System.DateTime})
Sets the value of the calendar

### Value(System.String)
Sets the value of the calendar

### Selection(System.Action{Kendo.Mvc.UI.Fluent.CalendarSelectionSettingsBuilder})
Configures the selection settings of the calendar.

#### Parameters

##### selectionAction `System.Action{Kendo.Mvc.UI.Fluent.CalendarSelectionSettingsBuilder}`
SelectAction settings, which includes Action name and IEnumerable of DateTime objects.

#### Parameters

##### selectionAction `System.Action{Kendo.Mvc.UI.Fluent.CalendarSelectionSettingsBuilder}`
SelectAction settings, which includes Action name and IEnumerable of DateTime objects.