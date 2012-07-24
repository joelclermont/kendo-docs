---
title: DatePicker
slug: datepicker
publish: true
---

# Server-Side API

Defining min and max dates:

#### Old
    
    Html.Telerik().Calendar().Name("Calendar").MinDate(DateTime.Now)
    Html.Telerik().Calendar().Name("Calendar").MaxDate(DateTime.Now)

#### New

    Html.Kendo().Calendar().Name("Calendar").Min(DateTime.Now)
    Html.Kendo().Calendar().Name("Calendar").Max(DateTime.Now)

Footer:

#### Old

    Html.Telerik().Calendar().Name("Calendar").TodayButton(“d”)

#### New
    
    Html.Kendo().Calendar().Name("Calendar").Footer(“#= kendo.toString(data, ‘MM/dd/yyyy’)”)

howButton and ButtonTitle:

#### Old
    
    Html.Telerik().DatePicker().Name("Calendar").ButtonTitle(“choose date”)
    Html.Telerik().DatePicker().Name("Calendar").ShowButton(false)

#### New

    Not Supported

**OpenOnFocus**:

#### Old

    Html.Telerik().DatePicker ().Name("Calendar").OpenOnFocus(true)

#### New
    
    Not Supported

# Client-Side API

## Events

All events no longer have the “On” prefix.

All widgets no longer have the OnLoad event. Please use **$(document).ready()** instead.

### Disable

#### Old

    var datePicker = $("#DatePicker").data("tDatePicker");
    datePicker.disable();

#### New
    
    var datePicker = $("#datepicker").data("kendoDatePicker");
    datePicker.enable(false);
