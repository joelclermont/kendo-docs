# kendo.ui.DateTimePicker

## Description

 The **DateTimePicker** allows the end user to select a value from a
 calendar or a time drop-down list. Direct input is also allowed.
 It supports configurable options for minimum and maximum value, the format,
 the interval between predefined hours in the time view, custom templates for "month" view
 of the calendar, start view and the depth of the navigation.


### Getting Started

#### Creating a DateTimePicker from existing input element

    <input id="dateTimePicker" />

#### DateTimePicker initialization

    $(document).ready(function(){
     $("#dateTimePicker").kendoDateTimePicker();
    }); When a **DateTimePicker** is initialized, it will be displayed at the
 location of the target HTML element.


### Configuring DateTimePicker Behaviors


 The **DateTimePicker** provides configuration options that can be set
 during initialization. Among the properties that can be controlled:


*   Selected datetime
*   Minimum/Maximum datetime
*   Define format
*   Start view
*   Navigation depth (last view to which end user can navigate)
*   Define interval between predefined values in the time drop-down list

#### Create DateTimePicker with a selected value and a defined
minimum and maximum datetime

    $(document).ready(function(){
     $("#dateTimePicker").kendoDateTimePicker({
        value: new Date(2000, 10, 10, 10, 0, 0),
        min: new Date(1950, 0, 1, 8, 0, 0),
        max: new Date(2049, 11, 31, 18, 0, 0)
     })
    }); DateTimePicker will set the value only if the entered datetime is valid and
 within the defined range.

#### Define the format

    $("#dateTimePicker").kendoDateTimePicker({
        format: "MM/dd/yyyy hh:mm tt" //format is used to format the value of the widget and to parse the input.
    });

#### Define the time format

    $("#dateTimePicker").kendoDateTimePicker({
        timeFormat: "hh:mm:ss tt" //this format will be used to format the predefined values in the time list.
    });### Defining a Start View and Navigation Depth


 The first rendered view can be defined with "start" option.
 Navigation depth can be controlled with "depth" option. Predefined
 views are:


*   "month" - shows the days from the month
*   "year" - shows the months of the year
*   "decade" - shows the years from the decade
*   "century" - shows the decades from the century

#### Create a DateTimePicker for selecting a month

    $("#dateTimePicker").kendoDateTimePicker({
     start: "year",
     depth: "year"
    });

#### Define the interval (in minutes) between values in the time drop-down list

    $("#dateTimePicker").kendoDateTimePicker({
        interval: 15
    })### Accessing an Existing DateTimePicker


 You can reference an existing **DateTimePicker** instance via
 [jQuery.data()](http://api.jquery.com/jQuery.data/).
 Once a reference has been established, you can use the API to control
 its behavior.

#### Accessing an existing DateTimePicker instance

    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");

## Configuration

### `animation` : **Object** 

The animation(s) used for opening and/or closing the pop-ups. Setting this value to **false**
will disable the animation(s).

### `animation.close` : **Object** 

The animation(s) used for hiding of the pop-up.

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        animation: {
            close: {
                effects: "fadeOut",
                duration: 300,
                show: false,
                hide: true
            }
        }
    });

### `animation.open` : **Object** 

The animation(s) used for displaying of the pop-up.

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        animation: {
            open: {
                effects: "fadeIn",
                duration: 300,
                show: true
            }
        }
    });

### `culture` : **String** *(default: en-US)*

 Specifies the culture info used by the widget.

#### Example

    // specify on widget initialization
    $("#datetimepicker").kendoDateTimePicker({
        culture: "de-DE"
    });

### `dates` : **Array** 

 Specifies a list of dates, which are shown in the time drop-down list. If not set, the DateTimePicker will auto-generate the available times.
 

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        dates: [new Date(2000, 10, 10, 10, 0, 0), new Date(2000, 10, 10, 30, 0)] //the drop-down list will consist only two entries - "10:00 AM" and "10:30 AM"
    });

### `depth` : **String** 

Specifies the navigation depth of the calendar. The following
settings are available for the **depth** value:
<div class="details-list">
   <dl>
        <dt>
             `"month"`
        </dt>
        <dd>
            shows the days of the month
        </dd>
        <dt>
             `"year"`
        </dt>
        <dd>
             shows the months of the year
        </dd>
        <dt>
             `"decade"`
        </dt>
        <dd>
             shows the years of the decade
        </dd>
        <dt>
             `"century"`
        </dt>
        <dd>
             shows the decades from the centery
        </dd>
   </dl>
</div>

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        start: "decade",
        depth: "year" // the dateTimePicker will only go to the year level
    });

### `footer` : **String** 

 Template to be used for rendering the footer of the calendar.

#### Example

    // DateTimePicker initialization
     <script>
         $("#dateTimePicker").kendoDateTimePicker({
             footer: kendo.template("Today - #=kendo.toString(data, 'd') #")
         });
     </script>

### `format` : **String** *(default: MM/dd/yyyy h:mm tt)*

 Specifies the format, which is used to format the value of the DateTimePicker displayed in the input.

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        format: "yyyy/MM/dd hh:mm tt"
    });

### `interval` : **Number** *(default: 30)*

 Specifies the interval, between values in the popup list, in minutes.

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        interval: 15
    });

### `max` : **Date** *(default: Date(2099, 11, 31))*

 Specifies the maximum date, which the calendar can show.

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
     max: new Date(2013, 0, 1) // sets max date to Jan 1st, 2013 12:00 AM
    });

#### Example

    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    // set the max date to Jan 1st, 2013 12:00 AM
    dateTimePicker.max(new Date(2013,0, 1));

### `min` : **Date** *(default: Date(1900, 0, 1))*

 Specifies the minimum date that the calendar can show.

#### Example

    // set the min date to Jan 1st, 2011
    $("#dateTimePicker").kendoDateTimePicker({
     min: new Date(2011, 0, 1)
    });

#### Example

    // get a reference to the dateTimePicker widget
    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    // set the min date to Jan 1st, 2011 12:00 AM
    dateTimePicker.min(new Date(2011, 0, 1));

### `month` : **Object** 

 Templates for the cells rendered in the calendar "month" view.

### `month.content` : **String** 

 Template to be used for rendering the cells in the calendar "month" view, which are in range.

#### Example

    //template
    <script id="cellTemplate" type="text/x-kendo-tmpl">
         <div class="${ data.value < 10 ? exhibition : party }">
         </div>
         ${ data.value }
     </script>
    
     //dateTimePicker initialization
     <script>
         $("#dateTimePicker").kendoDateTimePicker({
             month: {
                content:  kendo.template($("#cellTemplate").html()),
             }
         });
     </script>

### `month.empty` : **String** 

The template used for rendering the cells in the calendar "month" view, which are not in the range between
the minimum and maximum values.

### `parseFormats` : **Array** 

 Specifies the formats, which are used to parse the value set with value() method or by direct input. If not set the value of the options.format and options.timeFormat will be used.

#### Example

    $("#datePicker").kendoDatePicker({
        format: "yyyy/MM/dd hh:mm tt",
        parseFormats: ["MMMM yyyy", "HH:mm"] //format also will be added to parseFormats
    });

### `start` : **String** *(default: month)*

 Specifies the start view of the calendar.
The following settings are available for the **start** value:
<div class="details-list">
   <dl>
        <dt>
             `"month"`
        </dt>
        <dd>
            shows the days of the month
        </dd>
        <dt>
             `"year"`
        </dt>
        <dd>
             shows the months of the year
        </dd>
        <dt>
             `"decade"`
        </dt>
        <dd>
             shows the years of the decade
        </dd>
        <dt>
             `"century"`
        </dt>
        <dd>
             shows the decades from the centery
        </dd>
   </dl>
</div>

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        start: "decade" // the dateTimePicker will start with a decade display
    });

### `timeFormat` : **String** *(default: h:mm tt)*

 Specifies the format, which is used to format the values in the time drop-down list.

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        timeFormat: "HH:mm" //24 hours format
    });

### `value` : **Date** *(default: null)*

 Specifies the selected value.

#### Example

    // set the selected value to January 1st, 2011 12:00 AM
    $("#dateTimePicker").kendoDateTimePicker({
     value: new Date(2011, 0, 1)
    });

#### Example

    // get a reference to the dateTimePicker widget
    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    // set the selected value on the dateTimePicker to January 1st, 2011
    dateTimePicker.value(new Date(2011, 0, 1));

## Methods

### close

Closes the calendar or the time drop-down list.

#### Close the calendar of the DateTimePicker

    $("dateTimePicker").data("kendoDateTimePicker").close();

#### Close the calendar of the DateTimePicker

    $("dateTimePicker").data("kendoDateTimePicker").close("date");

#### Close the time drop-down list of a DateTimePicker.

    $("dateTimePicker").data("kendoDateTimePicker").close("time");

#### Parameters

##### view `String`

The view of the DateTimePicker, expressed as a string.
Available views are "time" and "date".

### enable

Enables or disables a DateTimePicker.

#### Enable a DateTimePicker

    $("dateTimePicker").data("kendoDateTimePicker").enable();

#### Enable a dateTimePicker

    $("dateTimePicker").data("kendoDateTimePicker").enable(true);

#### Disable a dateTimePicker

    $("dateTimePicker").data("kendoDateTimePicker").enable(false);

#### Parameters

##### enable `Boolean`

Enables (**true** or undefined) or disables (**false**) a DateTimePicker.

### max

Gets or sets the maximum value of the DateTimePicker.

#### Get the maximum value of a DateTimePicker

    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    var maximum = dateTimePicker.max();

#### Set the maximum value of a DateTimePicker

    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    dateTimePicker.max(new Date(1900, 0, 1, 10, 0, 0));

#### Parameters

##### value `Date|String`

The maximum time value to set for a DateTimePicker, expressed as a Date object or as a string.

#### Returns

`Date` The maximum time value of a DateTimePicker.

### min

Gets or sets the minimum value of the DateTimePicker.

#### Get the minimum value of a DateTimePicker

    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    var minimum = dateTimePicker.min();

#### Set the minimum value of a DateTimePicker

    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    dateTimePicker.min(new Date(1900, 0, 1, 10, 0, 0));

#### Parameters

##### value `Date|String`

The minimum time value to set for a DateTimePicker, expressed as a Date object or as a string.

#### Returns

`Date` The minimum time value of a DateTimePicker.

### open

Opens the calendar or the time drop-down list.

#### Open the calendar of the DateTimePicker

    $("dateTimePicker").data("kendoDateTimePicker").open();

#### Open the calendar of the DateTimePicker

    $("dateTimePicker").data("kendoDateTimePicker").open("date");

#### Open the time drop-down list of a DateTimePicker.

    $("dateTimePicker").data("kendoDateTimePicker").open("time");

#### Parameters

##### view `String`

The view of the DateTimePicker, expressed as a string.
Available views are "time" and "date".

### toggle

Toggles the calendar or the time drop-down list.

#### Toggle the calendar of the DateTimePicker

    $("dateTimePicker").data("kendoDateTimePicker").toggle();

#### Toggle the calendar of the DateTimePicker

    $("dateTimePicker").data("kendoDateTimePicker").toggle("date");

#### Toggle the time drop-down list of a DateTimePicker.

    $("dateTimePicker").data("kendoDateTimePicker").toggle("time");

#### Parameters

##### view `String`

The view of the DateTimePicker, expressed as a string.
Available views are "time" and "date".

### value

Gets or sets the value of the DateTimePicker.

#### Get the value of a DateTimePicker

    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    var timePickerValue = dateTimePicker.value();

#### Set the value of a DateTimePicker

    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    dateTimePicker.value("2/23/2000 10:00 AM");

#### Parameters

##### value `Date|String`

The time value to set for a DateTimePicker, expressed as a Date object or as a string.

#### Returns

`Date` The time value of a DateTimePicker.

## Events

### change

Triggered when the underlying value of a DateTimePicker is changed.

#### Attach change event handler during initialization; detach via unbind()

    // event change for expand
    var onChange = function(e) {
        // ...
    };
    
    // attach change event handler during initialization
    var dateTimePicker = $("#dateTimePicker").kendoDateTimePicker({
        change: onChange
    });
    
    // detach change event handler via unbind()
    dateTimePicker.data("kendoDateTimePicker").unbind("change", onChange);

#### Attach change event handler via bind(); detach via unbind()

    // event change for expand
    var onChange = function(e) {
        // ...
    };
    
    // attach change event handler via bind()
    $("#dateTimePicker").data("kendoDateTimePicker").bind("change", onChange);
    
    // detach change event handler via unbind()
    $("#dateTimePicker").data("kendoDateTimePicker").unbind("change", onChange);

### close

Fires when the calendar or the time drop-down list is closed

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        close: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the dateTimePicker widget
    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    // bind to the close event
    dateTimePicker.bind("close", function(e) {
        // handle event
    });

### open

Fires when the calendar or the time drop-down list is opened

#### Example

    $("#dateTimePicker").kendoDateTimePicker({
        open: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the dateTimePicker widget
    var dateTimePicker = $("#dateTimePicker").data("kendoDateTimePicker");
    // bind to the open event
    dateTimePicker.bind("open", function(e) {
        // handle event
    });