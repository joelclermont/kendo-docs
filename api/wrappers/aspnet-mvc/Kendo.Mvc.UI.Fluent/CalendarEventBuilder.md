---
title:Kendo.Mvc.UI.Fluent.CalendarEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.calendareventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.CalendarEventBuilder

Defines the fluent interface for configuring datepicker client events.

## Methods

### Change(System.Func{System.Object,System.Object})
Defines the inline handler of the Change client-side event

#### Example
    <%= Html.Kendo().Calendar()
        .Name("DatePicker")
        .Events(events => events.Change(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        %>

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Navigate(System.Func{System.Object,System.Object})
Defines the inline handler of the Navigate client-side event

#### Example
    <%= Html.Kendo().Calendar()
        .Name("Calendar")
        .Events(events => events.Navigate(
        @<text>
        %>
        function(e) {
        //event handling code
        }
        </text>
        ))
        %>

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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