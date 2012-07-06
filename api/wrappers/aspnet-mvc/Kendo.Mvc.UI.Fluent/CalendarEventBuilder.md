---
title:Kendo.Mvc.UI.Fluent.CalendarEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.calendareventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.CalendarEventBuilder

## Methods

### Navigate(System.String)
Defines the name of the JavaScript function that will handle the Navigate client-side event.

#### Example
    <%= Html.Kendo().Calendar()
        .Name("Calendar")
        .Events(events => events.Navigate("navigate"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.