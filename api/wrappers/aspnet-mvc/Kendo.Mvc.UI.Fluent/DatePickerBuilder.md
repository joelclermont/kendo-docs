---
title:Kendo.Mvc.UI.Fluent.DatePickerBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.datepickerbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.DatePickerBuilder

Defines the fluent interface for configuring the DatePicker component.

## Methods

### FooterId(System.String)
FooterId to be used for rendering the footer of the Calendar.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .FooterId("widgetFooterId")
        %>

### Footer(System.String)
Footer template to be used for rendering the footer of the Calendar.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Footer("#= kendo.toString(data, "G") #")
        %>

### Depth(Kendo.Mvc.UI.CalendarView)
Specifies the navigation depth.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Depth(CalendarView.Month)
        %>

### Start(Kendo.Mvc.UI.CalendarView)
Specifies the start view.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .Start(CalendarView.Month)
        %>

### MonthTemplateId(System.String)
MonthTemplateId to be used for rendering the cells of the Calendar.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .MonthTemplateId("widgetMonthTemplateId")
        %>

### MonthTemplate(System.String)
Templates for the cells rendered in the "month" view.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .MonthTemplate("#= data.value #")
        %>

### MonthTemplate(System.Action{Kendo.Mvc.UI.Fluent.MonthTemplateBuilder})
Configures the content of cells of the Calendar.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        .MonthTemplate(month => month.Content("#= data.value #"))
        %>

### Min(System.String)
Sets the minimal date, which can be selected in DatePicker.

### Max(System.String)
Sets the maximal date, which can be selected in DatePicker.