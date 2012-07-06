---
title:Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.datepickereventbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase

## Methods

### Change(System.Func{System.Object,System.Object})
Defines the inline handler of the Change client-side event

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events => events.Change(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### Change(System.String)
Defines the name of the JavaScript function that will handle the the Change client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events => events.Change("change"))
        %>

### Open(System.Func{System.Object,System.Object})
Defines the inline handler of the Open client-side event

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events => events.Open(
        @<text>
        %>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### Open(System.String)
Defines the name of the JavaScript function that will handle the Open client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events => events.Open("open"))
        %>

### Close(System.Func{System.Object,System.Object})
Defines the inline handler of the Close client-side event

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events => events.Close(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### Close(System.String)
Defines the name of the JavaScript function that will handle the Close client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events => events.Close("close"))
        %>