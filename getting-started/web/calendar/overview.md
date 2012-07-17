---
title: Calendar Overview
slug: calendar-overview
tags: getting-started,web
publish: true
---

# Calendar Overview

The **Calendar** renders a graphical calendar that supports
navigation and selection. It supports custom templates for its
"month" view, configurable options for a minimum and maximum date,
start view and the depth of the navigation.

## Getting Started

### Create a div element

    <div id="calendar"></div>

### Initialize the Calendar via a jQuery ID selector

    $(document).ready(function(){
        $("#calendar").kendoCalendar();
    });

When a **Calendar** is initialized, it will automatically be
displayed near the location of the used HTML element.


## Configuring Calendar Behaviors


The **Calendar** provides many configuration options that can be
easily set during initialization. Among the properties that can be
controlled:


*   Selected date
*   Minimum and/or maximum date
*   Start view
*   Define the navigation depth (last view to which end user can
navigate)
*   Day template
*   Footer template

### Create Calendar with selected date and a defined minimum
and maximum date

    $("#calendar").kendoCalendar({
        value: new Date(),
        min: new Date(1950, 0, 1),
        max: new Date(2049, 11, 31)
    });

The **Calendar** will not navigate before than the minimum
date specified. It will also not navigate ahead the maximum date
specified.

## Define start view and navigation depth


The first rendered view can be defined with "start" option.
Navigation depth can be controlled with "depth" option. Predefined
views are:


*   "month" - shows the days from the month
*   "year" - shows the months of the year
*   "decade" - shows the years from the decade
*   "century" - shows the decades from the century

### Create a Calendar, which allows a user to select a month

    $("#calendar").kendoCalendar({
        start: "year",
        depth: "year"
    });

## Customize day template


The **Calendar** allows to customize content of the rendered day
in the "month" view.

### Create a Calendar with custom template

    $("#calendar").kendoCalendar({
        month: {
            content: '<div class="custom"><#=data.value#></div>'
        }
    });

This templates wraps the "value" in a div HTML element. Here is an
example of the object passed to the template function:

### Structure of the data object passed to the template

    data = {
        date: date, // Date object corresponding to the current cell
        title: kendo.toString(date, "D"),
        value: date.getDate(),
        dateString: "2011/0/1" // formatted date using yyyy/MM/dd format and month is zero-based
    };

## Accessing an Existing Calendar


You can reference an existing **Calendar** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the API to control
its behavior.

### Accessing an existing Calendar instance

    var calendar = $("#calendar").data("kendoCalendar");

