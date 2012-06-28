---
title: kendo.ui.Calendar
tags: api,web
publish: true
---

# kendo.ui.Calendar

## Description



The **Calendar** renders a graphical calendar that supports
navigation and selection. It supports custom templates for its
"month" view, configurable options for a minimum and maximum date,
start view and the depth of the navigation.


### Getting Started

#### Create a div element

    <div id="calendar"></div>

#### Initialize the Calendar via a jQuery ID selector

    $(document).ready(function(){
     $("#calendar").kendoCalendar();
    });

When a **Calendar** is initialized, it will automatically be
displayed near the location of the used HTML element.


### Configuring Calendar Behaviors


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

#### Create Calendar with selected date and a defined minimum
and maximum date

    $("#calendar").kendoCalendar({
     value: new Date(),
     min: new Date(1950, 0, 1),
     max: new Date(2049, 11, 31)
    });

The **Calendar** will not navigate before than the minimum
date specified. It will also not navigate ahead the maximum date
specified.

### Define start view and navigation depth


The first rendered view can be defined with "start" option.
Navigation depth can be controlled with "depth" option. Predefined
views are:


*   "month" - shows the days from the month
*   "year" - shows the months of the year
*   "decade" - shows the years from the decade
*   "century" - shows the decades from the century

#### Create a Calendar, which allows a user to select a month

    $("#calendar").kendoCalendar({
     start: "year",
     depth: "year"
    });

### Customize day template


The **Calendar** allows to customize content of the rendered day
in the "month" view.

#### Create a Calendar with custom template

    $("#calendar").kendoCalendar({
     month: {
      content: '<div class="custom"><#=data.value#></div>'
     }
    });

This templates wraps the "value" in a div HTML element. Here is an
example of the object passed to the template function:

#### Structure of the data object passed to the template

    data = {
     date: date, // Date object corresponding to the current cell
     title: kendo.toString(date, "D"),
     value: date.getDate(),
     dateString: "2011/0/1" // formatted date using yyyy/MM/dd format and month is zero-based
    };

### Accessing an Existing Calendar


You can reference an existing **Calendar** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the API to control
its behavior.

#### Accessing an existing Calendar instance

    var calendar = $("#calendar").data("kendoCalendar");

## Configuration

### culture `String`*(default: en-US)*

 Specifies the culture info used by the widget.

#### Example

    // specify on widget initialization
    $("#calendar").kendoCalendar({
        culture: "de-DE"
    });

### dates `Array`

 Specifies a list of dates, which will be passed to the month template.
 

#### Example

    $("#calendar").kendoCalendar({
        dates: [new Date(2000, 10, 10, 10, 0, 0), new Date(2000, 10, 10, 30, 0)] //can manipulate month template depending on this array.
    });

### depth `String`

Specifies the navigation depth.

#### Example

    $("#calendar").kendoCalendar({
        depth: "year"
    });

### footer `String`

 Specifies the content of the footer. If false, the footer will not be rendered.

#### Example

    // change the footer text from the default current date
    $("#calendar").kendoCalendar({
        footer = "My Custom Footer"
    });

#### Example

    $("#calendar").kendoCalendar({
        footer = false;
    });

### footer `String`

 Template to be used for rendering the footer. If false, the footer will not be rendered.

#### Example

    //calendar intialization
     <script>
         $("#calendar").kendoCalendar({
             footer: kendo.template("Today - #=kendo.toString(data, 'd') #")
         });
     </script>

### format `String`*(default: MM/dd/yyyy)*

 Specifies the format, which is used to parse value set with value() method.

#### Example

    $("#calendar").kendoCalendar({
        format: "yyyy/MM/dd"
    });

### max `Date`*(default: Date(2099, 11, 31))*

 Specifies the maximum date, which the calendar can show.

#### Example

    $("#calendar").kendoCalendar({
        max = new Date(2013, 0, 1);
    });

#### Example

    // get a reference to the Kendo UI calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // set the max date to Jan 1st, 2013
    calendar.max(new Date(2013, 0, 1));

### min `Date`*(default: Date(1900, 0, 1))*

 Specifies the minimum date, which the calendar can show.

#### Example

    // set the min date to Jan 1st, 2011
    $("#calendar").kendoCalendar({
        min = new Date(2011, 0, 1)
    });

#### Example

    // get a reference to the Kendo UI calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // set the min date to Jan 1st, 2011
    calendar.min(new Date(2011, 0, 1));

### month `Object`

 Templates for the cells rendered in the "month" view.

### month.content `String`

 Template to be used for rendering the cells in the "month" view, which are in range.

#### Example

    //template
    <script id="cellTemplate" type="text/x-kendo-tmpl">
         <div class="${ data.value < 10 ? exhibition : party }">
         </div>
         ${ data.value }
     </script>
    
     //calendar intialization
     <script>
         $("#calendar").kendoCalendar({
             month: {
                content:  kendo.template($("#cellTemplate").html()),
             }
         });
     </script>

### month.empty `String`

 Template to be used for rendering the cells in the "month" view, which are not in the min/max range.

### start `String`*(default: month)*

 Specifies the start view.

#### Example

    $("#calendar").kendoCalendar({
        start: "year"
    });

### value `Date`*(default: null)*

 Specifies the selected date.

#### Example

    // set the selected date to Jan 1st. 2012
    $("#calendar").kendoCalendar({
        value: new Date(2012, 0, 1)
    });

#### Example

    // get a reference to the Kendo UI calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // set the selected date on the calendar to Jan 1st, 2012
    calendar.value(new Date(2012, 0, 1));

## Methods

### max

Gets/Sets the max value of the calendar.

#### Example

    // get a reference to the calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    
    // get the max value of the calendar.
    var max = calendar.max();
    
    // set the max value of the calendar.
    calendar.max(new Date(2100, 0, 1));

#### Parameters

##### value `Date | String`

The max date to set.

#### Returns

`Date` The max value of the calendar.

### min

Gets/Sets the min value of the calendar.

#### Example

    // get a reference to the calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    
    // get the min value of the calendar.
    var min = calendar.min();
    
    // set the min value of the calendar.
    calendar.min(new Date(1900, 0, 1));

#### Parameters

##### value `Date|String`

The min date to set.

#### Returns

`Date` The min value of the calendar.

### navigate

Navigates to view

#### Example

    // get a reference to the calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // navigate to the desired date
    calendar.navigate(value, view);

#### Parameters

##### value `Date`

Desired date

##### view `String`

Desired view

### navigateDown

Navigates to the lower view

#### Example

    // get a reference to the calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // navigate down
    calendar.navigateDown(value);

#### Parameters

##### value `Date`

Desired date

### navigateToFuture

Navigates to the future

#### Example

    // get a reference to the calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // navigate to future
    calendar.navigateToFuture();

### navigateToPast

Navigates to the past

#### Example

    // get a reference to the calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // navigate to past
    calendar.navigateToPast();

### navigateUp

Navigates to the upper view

#### Example

    // get a reference to the calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // navigate up
    calendar.navigateUp();

### value

Gets/Sets the value of the calendar.

#### Example

    // get a reference to the calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    
    // get the value of the calendar.
    var value = calendar.value();
    
    // set the value of the calendar.
    calendar.value(new Date());

#### Parameters

##### value `Date|String`

The date to set.

#### Returns

`Date` The value of the calendar.

## Events

### change

Fires when the selected date is changed

#### Example

    $("#calendar").kendoCalendar({
        change: function(e) {
            // handle event
        });
    });

#### To set after initialization

    // get a reference to the Kendo UI calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // bind to the change event
    calendar.bind("change", function(e) {
         // handle event
    });

### navigate

Fires when navigate

#### Example

    $("#calendar").kendoCalendar({
        navigate: function(e) {
             // handle event
        }
    });

#### To set after initialization

    // get a reference to the Kendo UI calendar widget
    var calendar = $("#calendar").data("kendoCalendar");
    // bind to the change event
    calendar.bind("navigate", function(e) {
         // handle event
    });