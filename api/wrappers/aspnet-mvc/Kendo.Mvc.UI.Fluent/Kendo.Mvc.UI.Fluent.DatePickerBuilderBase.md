---
title:Kendo.Mvc.UI.Fluent.DatePickerBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.datepickerbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.DatePickerBuilderBase

## Methods

### Events(System.Action{Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase})
Configures the client-side events.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events =>
        events.Open("open").Change("change")
        )
        %>

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase}`
The client events action.

### Format(System.String)
Sets the date format, which will be used to parse and format the machine date.

### Enable(System.Boolean)
Enables or disables the picker.

### Min(System.DateTime)
Sets the minimal date, which can be selected in picker.

### Max(System.DateTime)
Sets the maximal date, which can be selected in picker.

### Value(System.Nullable{System.DateTime})
Sets the value of the picker input

### Value(System.String)
Sets the value of the picker input