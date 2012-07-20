---
title: Calendar
slug: calendar
publish: true
---

## Server-Side API

## Events

### Old

    Html.Telerik().Calendar().Name("Calendar").ClientEvents( events => events.OnChange(“change”))
 
### New

    Html.Kendo().Calendar().Name("Calendar").Events( events => events.Change(“change”))

## Other Options

### Min/Max date
 
#### Old

    Html.Telerik().Calendar().Name("Calendar").MinDate(DateTime.Now)
    Html.Telerik().Calendar().Name("Calendar").MaxDate(DateTime.Now)
 
#### New

    Html.Kendo().Calendar().Name("Calendar").Min(DateTime.Now)
    Html.Kendo().Calendar().Name("Calendar").Max(DateTime.Now)

### Footer
 
#### Old

    Html.Telerik().Calendar().Name("Calendar").TodayButton(“d”)
 
#### New

    Html.Kendo().Calendar().Name("Calendar").Footer(“#= kendo.toString(data, ‘MM/dd/yyyy’)”)