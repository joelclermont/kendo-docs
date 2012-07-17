---
title: TimePicker Overview
slug: getting-started.web.timepicker
tags: getting-started,web
publish: true
---

# TimePicker Overview

The **TimePicker** allows the end user to select a time value from a list of predefined values or
to type a new value. It supports configurable options for the format, minimum and maximum time, and the
interval between predefined values in the list.


## Getting Started

### Creating a TimePicker from existing input element

    <input id="timePicker" />

### Initialize the PanelBar via an ID selector

    $(document).ready(function(){
        $("#timePicker").kendoTimePicker();
    });

When a **TimePicker** is initialized, it will automatically be displayed near the location of the
used HTML element.


## Configuring TimePicker Behaviors


A **TimePicker** provides configuration options that can be easily set during initialization.
Among the properties that can be controlled:


*   Selected time
*   Minimum/Maximum time
*   Define format
*   Define interval between predefined values in the list

### Create TimePicker with selected time and defined min and max time

    $("#timePicker").kendoTimePicker({
        value: new Date(2000, 10, 10, 10, 0, 0),
        min: new Date(1950, 0, 1, 8, 0, 0),
        max: new Date(2049, 11, 31, 18, 0, 0)
    });

A **TimePicker** will set the value only if the entered time is valid and if it is in the defined
range.

### Define time format

    $("#timePicker").kendoTimePicker({
        format: "hh:mm:ss tt"
    });

### Define the interval (in minutes) between values in the list

    $("#timePicker").kendoTimePicker({
        interval: 15
    });

## Accessing an Existing TimePicker


You can reference an existing **TimePicker** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

### Accessing an existing TimePicker instance

    var timePicker = $("#timePicker").data("kendoTimePicker");

