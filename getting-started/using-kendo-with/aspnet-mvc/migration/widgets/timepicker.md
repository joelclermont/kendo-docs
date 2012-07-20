---
title: TimePicker
slug: timepicker
publish: true
---

# Server-Side API

## Defining Min and Max dates

### Old

    Html.Telerik().Calendar().Name("Calendar").MinDate(DateTime.Now)
    Html.Telerik().Calendar().Name("Calendar").MaxDate(DateTime.Now)

### New
    
    Html.Kendo().Calendar().Name("Calendar").Min(DateTime.Now)
    Html.Kendo().Calendar().Name("Calendar").Max(DateTime.Now)

## Footer

### Old
    
    Html.Telerik().Calendar().Name("Calendar").TodayButton(“d”)

### New
    
    Html.Kendo().Calendar().Name("Calendar").Footer(“#= kendo.toString(data, ‘MM/dd/yyyy’)”)

# Client-Side API

## Events

All events no longer have the “On” prefix.

All widgets no longer have the OnLoad event. Please use **$(document).ready()** instead.

## Disable

### Old

    var datePicker = $("#DatePicker").data("tTimePicker");
    datePicker.disable();

### New

    var datePicker = $("#datepicker").data("kendoTimePicker");
    datePicker.enable(false);
