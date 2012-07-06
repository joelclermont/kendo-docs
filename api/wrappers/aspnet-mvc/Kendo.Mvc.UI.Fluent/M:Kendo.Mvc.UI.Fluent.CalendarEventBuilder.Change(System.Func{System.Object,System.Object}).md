---
title:Kendo.Mvc.UI.Fluent.CalendarEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.calendareventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.CalendarEventBuilder

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