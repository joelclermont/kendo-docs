---
title:DateTimePickerBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.datetimepickerbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.DateTimePickerBuilder

Defines the fluent interface for configuring the TimePicker component.

## Methods

### Interval(System.Int32)
Sets the interval between hours.

### Footer(System.String)
Footer template to be used for rendering the footer of the Calendar.

#### Example
    <%= Html.Kendo().DateTimePicker()
        .Name("DateTimePicker")
        .Footer("#= kendo.toString(data, "G") #")
        %>

### FooterId(System.String)
FooterId to be used for rendering the footer of the Calendar.

#### Example
    <%= Html.Kendo().DateTimePicker()
        .Name("DateTimePicker")
        .FooterId("widgetFooterId")
        %>

### Depth(Kendo.Mvc.UI.CalendarView)
Specifies the navigation depth.

#### Example
    <%= Html.Kendo().DateTimePicker()
        .Name("DateTimePicker")
        .Depth(CalendarView.Month)
        %>

### Start(Kendo.Mvc.UI.CalendarView)
Specifies the start view.

#### Example
    <%= Html.Kendo().DateTimePicker()
        .Name("DateTimePicker")
        .Start(CalendarView.Month)
        %>

### MonthTemplateId(System.String)
MonthTemplateId to be used for rendering the cells of the Calendar.

#### Example
    <%= Html.Kendo().DateTimePicker()
        .Name("DateTimePicker")
        .MonthTemplateId("widgetMonthTemplateId")
        %>

### MonthTemplate(System.String)
Templates for the cells rendered in the "month" view.

#### Example
    <%= Html.Kendo().DateTimePicker()
        .Name("DateTimePicker")
        .MonthTemplate("#= data.value #")
        %>

### MonthTemplate(System.Action\<Kendo.Mvc.UI.Fluent.MonthTemplateBuilder\>)
Configures the content of cells of the Calendar.

#### Example
    <%= Html.Kendo().DateTimePicker()
        .Name("DateTimePicker")
        .MonthTemplate(month => month.Content("#= data.value #"))
        %>

### Min(System.String)
Sets the minimal date, which can be selected in DatePicker.

### Max(System.String)
Sets the maximal date, which can be selected in DatePicker.