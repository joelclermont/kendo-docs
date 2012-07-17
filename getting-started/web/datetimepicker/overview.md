---
title: DateTimePicker Overview
slug: getting-started.web.datetimepicker
tags: getting-started,web
publish: true
---

# DateTimePicker Overview

The **DateTimePicker** allows the end user to select a value from a
calendar or a time drop-down list. Direct input is also allowed.
It supports configurable options for minimum and maximum value, the format,
the interval between predefined hours in the time view, custom templates for "month" view
of the calendar, start view and the depth of the navigation.


## Getting Started

### Creating a DateTimePicker from existing input element

    <input id="dateTimePicker" />

### DateTimePicker initialization

    $(document).ready(function(){
        $("#dateTimePicker").kendoDateTimePicker();
    });

When a **DateTimePicker** is initialized, it will be displayed at the
location of the target HTML element.


## Configuring DateTimePicker Behaviors


The **DateTimePicker** provides configuration options that can be set
during initialization. Among the properties that can be controlled:


*   Selected datetime
*   Minimum/Maximum datetime
*   Define format
*   Start view
*   Navigation depth (last view to which end user can navigate)
*   Define interval between predefined values in the time drop-down list

### Create DateTimePicker with a selected value and a defined
minimum and maximum datetime

    $(document).ready(function(){
        $("#dateTimePicker").kendoDateTimePicker({
           value: new Date(2000, 10, 10, 10, 0, 0),
           min: new Date(1950, 0, 1, 8, 0, 0),
           max: new Date(2049, 11, 31, 18, 0, 0)
        })
    });

DateTimePicker will set the value only if the entered datetime is valid and
within the defined range.

### Define the format

    $("#dateTimePicker").kendoDateTimePicker({
        format: "MM/dd/yyyy hh:mm tt" //format is used to format the value of the widget and to parse the input.
    });

### Define the time format

    $("#dateTimePicker").kendoDateTimePicker({
        timeFormat: "hh:mm:ss tt" //this format will be used to format the predefined values in the time list.
    });

## Defining a Start View and Navigation Depth


The first rendered view can be defined with "start" option.
Navigation depth can be controlled with "depth" option. Predefined
views are:


*   "month" - shows the days from the month
*   "year" - shows the months of the year
*   "decade" - shows the years from the decade
*   "century" - shows the decades from the century

### Create a DateTimePicker for selecting a month

    $("#dateTimePicker").kendoDateTimePicker({
        start: "year",
        depth: "year"
    });

### Define the interval (in minutes) between values in the time drop-down list

    $("#dateTimePicker").kendoDateTimePicker({
        interval: 15
    })

## Accessing an Existing DateTimePicker


You can reference an existing **DateTimePicker** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the API to control
its behavior.

### Accessing an existing DateTimePicker instance

    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");

