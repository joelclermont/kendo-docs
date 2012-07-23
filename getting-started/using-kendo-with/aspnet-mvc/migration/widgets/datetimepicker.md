---
title: DateTimePicker
slug: datetimepicker
publish: true
---

# Server-side API

### Defining Min and Max Dates

#### Old
    
    Html.Telerik().Calendar().Name("Calendar").MinDate(DateTime.Now)
    Html.Telerik().Calendar().Name("Calendar").MaxDate(DateTime.Now)

#### New
    
    Html.Kendo().Calendar().Name("Calendar").Min(DateTime.Now)
    Html.Kendo().Calendar().Name("Calendar").Max(DateTime.Now)

### Footer

#### Old
    
    Html.Telerik().Calendar().Name("Calendar").TodayButton(“d”)

##3# New
    
    Html.Kendo().Calendar().Name("Calendar").Footer(“#= kendo.toString(data, ‘MM/dd/yyyy’)”)

### StartTime and EndTime

    Not implemented in Kendo UI

# Client-side API

## Events

All events no longer have the “On” prefix.

All widgets no longer have the OnLoad event. Please use $(document).ready() instead.

### Disable

#### Old
    
    var datePicker = $("#DatePicker").data("tDateTimePicker");
    datePicker.disable();

#### New
    
    var datePicker = $("#datepicker").data("kendoDateTimePicker");
    datePicker.enable(false);
