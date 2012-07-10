---
title:DatePickerEventBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.datepickereventbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase

Defines the fluent interface for configuring datepicker client events.

## Methods

### Change(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Change client-side event

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

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Change(System.String)
Defines the name of the JavaScript function that will handle the the Change client-side event.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events => events.Change("change"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Open(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Open client-side event

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

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Open(System.String)
Defines the name of the JavaScript function that will handle the Open client-side event.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events => events.Open("open"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Close(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Close client-side event

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

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Close(System.String)
Defines the name of the JavaScript function that will handle the Close client-side event.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events => events.Close("close"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.