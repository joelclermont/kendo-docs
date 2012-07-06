---
title:Kendo.Mvc.UI.Fluent.CalendarEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.calendareventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.CalendarEventBuilder

## Methods

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