---
title:Kendo.Mvc.UI.Fluent.CalendarEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.calendareventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.CalendarEventBuilder

## Methods

### Change(System.String)
Defines the name of the JavaScript function that will handle the the Change client-side event.

#### Example
    <%= Html.Kendo().Calendar()
        .Name("Calendar")
        .Events(events => events.Change("change"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.