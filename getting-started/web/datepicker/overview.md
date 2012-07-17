---
title: DatePicker Overview
slug: datepicker-overview
tags: getting-started,web
publish: true
---

# DatePicker Overview

The **DatePicker** allows the end user to select a date from a
calendar or by direct input. It supports custom templates for "month"
view, configurable options for min and max date, start view and the
depth of the navigation.


## Getting Started

### Creating a DatePicker from existing input element

    <input id="datePicker" />

### DatePicker initialization

    $(document).ready(function(){
        $("#datePicker").kendoDatePicker();
    });

When a **DatePicker** is initialized, it will be displayed at the
location of the target HTML element.


## Configuring DatePicker Behaviors


The **DatePicker** provides configuration options that can be set
during initialization. Among the properties that can be controlled:


*   Selected date
*   Minimum and/or maximum date
*   Define format
*   Start view
*   Navigation depth (last view to which end user can navigate)

### Create DatePicker with a selected date and a defined
minimum and maximum date

    $(document).ready(function(){
        $("#datePicker").kendoDatePicker({
           value: new Date(),
           min: new Date(1950, 0, 1),
           max: new Date(2049, 11, 31)
        })
    });

DatePicker will set the value only if the entered date is valid and
within the defined range.

## Defining a Start View and Navigation Depth


The first rendered view can be defined with "start" option.
Navigation depth can be controlled with "depth" option. Predefined
views are:


*   "month" - shows the days from the month
*   "year" - shows the months of the year
*   "decade" - shows the years from the decade
*   "century" - shows the decades from the century

### Create a DatePicker for selecting a month

    $("#datePicker").kendoDatePicker({
        start: "year",
        depth: "year"
    });

## Accessing an Existing DatePicker


You can reference an existing **DatePicker** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the API to control
its behavior.

### Accessing an existing DatePicker instance

    var datePicker = $("#datePicker").data("kendoDatePicker");

