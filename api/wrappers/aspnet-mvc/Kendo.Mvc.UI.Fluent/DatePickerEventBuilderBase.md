---
title:Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.datepickereventbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.DatePickerEventBuilderBase

## Methods

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