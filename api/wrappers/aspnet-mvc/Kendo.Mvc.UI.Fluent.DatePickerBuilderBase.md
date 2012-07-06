---
title:Kendo.Mvc.UI.Fluent.DatePickerBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.datepickerbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.DatePickerBuilderBase

## Methods

### 2.Events(System.Action{Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase})
Configures the client-side events.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase}`
The client events action.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase}`
The client events action.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Events(events =>
        events.Open("open").Change("change")
        )
        %>

### 2.Format(System.String)
Sets the date format, which will be used to parse and format the machine date.

### 2.Enable(System.Boolean)
Enables or disables the picker.

### 2.Min(System.DateTime)
Sets the minimal date, which can be selected in picker.

### 2.Max(System.DateTime)
Sets the maximal date, which can be selected in picker.

### 2.Value(System.Nullable{System.DateTime})
Sets the value of the picker input

### 2.Value(System.String)
Sets the value of the picker input