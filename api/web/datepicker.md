# kendo.ui.DatePicker

## Description



 The **DatePicker** allows the end user to select a date from a
 calendar or by direct input. It supports custom templates for "month"
 view, configurable options for min and max date, start view and the
 depth of the navigation.


### Getting Started

#### Creating a DatePicker from existing input element

    <input id="datePicker" />

#### DatePicker initialization

    $(document).ready(function(){
     $("#datePicker").kendoDatePicker();
    });

 When a **DatePicker** is initialized, it will be displayed at the
 location of the target HTML element.


### Configuring DatePicker Behaviors


 The **DatePicker** provides configuration options that can be set
 during initialization. Among the properties that can be controlled:


*   Selected date
*   Minimum and/or maximum date
*   Define format
*   Start view
*   Navigation depth (last view to which end user can navigate)

#### Create DatePicker with a selected date and a defined
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

### Defining a Start View and Navigation Depth


 The first rendered view can be defined with "start" option.
 Navigation depth can be controlled with "depth" option. Predefined
 views are:


*   "month" - shows the days from the month
*   "year" - shows the months of the year
*   "decade" - shows the years from the decade
*   "century" - shows the decades from the century

#### Create a DatePicker for selecting a month

    $("#datePicker").kendoDatePicker({
     start: "year",
     depth: "year"
    });

### Accessing an Existing DatePicker


 You can reference an existing **DatePicker** instance via
 [jQuery.data()](http://api.jquery.com/jQuery.data/).
 Once a reference has been established, you can use the API to control
 its behavior.

#### Accessing an existing DatePicker instance

    var datePicker = $("#datePicker").data("kendoDatePicker");

## Configuration

### `animation` : **Object** 

The animation(s) used for opening and/or closing the pop-up. Setting this value to **false**
will disable the animation(s).

### `animation.close` : **Object** 

The animation(s) used for hiding of the pop-up.

#### Example

    $("#datePicker").kendoDatePicker({
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

    $("#datePicker").kendoDatePicker({
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
    $("#datepicker").kendoDatePicker({
        culture: "de-DE"
    });

### `depth` : **String** 

Specifies the navigation depth. The following
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

    $("#datePicker").kendoDatePicker({
        start: "decade",
        depth: "year" // the datePicker will only go to the year level
    });

### `footer` : **String** 

 Template to be used for rendering the footer of the calendar.

#### Example

    // DatePicker initialization
     <script>
         $("#datePicker").kendoDatePicker({
             footer: kendo.template("Today - #=kendo.toString(data, 'd') #")
         });
     </script>

### `format` : **String** *(default: MM/dd/yyyy)*

 Specifies the format, which is used to format the value of the DatePicker displayed in the input.

#### Example

    $("#datePicker").kendoDatePicker({
        format: "yyyy/MM/dd"
    });

### `max` : **Date** *(default: Date(2099, 11, 31))*

 Specifies the maximum date, which the calendar can show.

#### Example

    $("#datePicker").kendoDatePicker({
     max: new Date(2013, 0, 1) // sets max date to Jan 1st, 2013
    });

#### Example

    var datePicker = $("#datePicker").data("kendoDatePicker");
    // set the max date to Jan 1st, 2013
    datePicker.max(new Date(2013,0, 1));

### `min` : **Date** *(default: Date(1900, 0, 1))*

 Specifies the minimum date that the calendar can show.

#### Example

    // set the min date to Jan 1st, 2011
    $("#datePicker").kendoDatePicker({
     min: new Date(2011, 0, 1)
    });

#### Example

    // get a reference to the datePicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    // set the min date to Jan 1st, 2011
    datePicker.min(new Date(2011, 0, 1));

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
    
     //datePicker initialization
     <script>
         $("#datePicker").kendoDatePicker({
             month: {
                content:  kendo.template($("#cellTemplate").html()),
             }
         });
     </script>

### `month.empty` : **String** 

The template used for rendering the cells in the calendar "month" view, which are not in the range between
the minimum and maximum values.

### `parseFormats` : **Array** 

 Specifies the formats, which are used to parse the value set with value() method or by direct input. If not set the value of the format will be used.

#### Example

    $("#datePicker").kendoDatePicker({
        format: "yyyy/MM/dd",
        parseFormats: ["MMMM yyyy"] //format also will be added to parseFormats
    });

### `start` : **String** *(default: month)*

 Specifies the start view.
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

    $("#datePicker").kendoDatePicker({
        start: "decade" // the datePicker will start with a decade display
    });

### `value` : **Date** *(default: null)*

 Specifies the selected date.

#### Example

    // set the selected value to January 1st, 2011
    $("#datePicker").kendoDatePicker({
     value: new Date(2011, 0, 1)
    });

#### Example

    // get a reference to the datePicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    // set the selected date on the datePicker to January 1st, 2011
    datePicker.value(new Date(2011, 0, 1));

## Methods

### close

Closes the calendar.

#### Example

    // get a reference to the datepicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    // close the datepicker
    datePicker.close();

### enable

Enable/Disable the datePicker widget.

#### Example

    // get a reference to the datepicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    
    // disables the datePicker
    datePicker.enable(false);
    
    // enables the datePicker
    datePicker.enable(true);

#### Parameters

##### enable `Boolean`

The argument, which defines whether to enable/disable the datePicker.

### max

Gets/Sets the max value of the datePicker.

#### Example

    // get a reference to the datepicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    
    // get the max value of the datePicker.
    var max = datePicker.max();
    
    // set the max value of the datePicker.
    datePicker.max(new Date(1900, 0, 1));

#### Parameters

##### value `Date | String`

The max date to set.

#### Returns

`Date` The max value of the datePicker.

### min

Gets/Sets the min value of the datePicker.

#### Example

    // get a reference to the datepicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    
    // get the min value of the datePicker.
    var min = datePicker.min();
    
    // set the min value of the datePicker.
    datePicker.min(new Date(1900, 0, 1));

#### Parameters

##### value `Date | String`

The min date to set.

#### Returns

`Date` The min value of the datePicker.

### open

Opens the calendar.

#### Example

    // get a reference to the datepicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    // open the datepicker
    datePicker.open();

### value

Gets/Sets the value of the datePicker.

#### Example

    // get a reference to the datepicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    
    // get the value of the datePicker.
    var value = datePicker.value();
    
    // set the value of the datePicker.
    datePicker.value("10/10/2000"); //parse "10/10/2000" date and selects it in the calendar.

#### Parameters

##### value `Date | String`

The value to set.

#### Returns

`Date` The value of the datePicker.

## Events

### change

Fires when the selected date is changed

#### Example

    $("#datePicker").kendoDatePicker({
        change: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the datePicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    // bind to the change event
    datePicker.bind("change", function(e) {
        // handle event
    });

### close

Fires when the calendar is closed

#### Example

    $("#datePicker").kendoDatePicker({
        close: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the datePicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    // bind to the close event
    datePicker.bind("close", function(e) {
        // handle event
    });

### open

Fires when the calendar is opened

#### Example

    $("#datePicker").kendoDatePicker({
        open: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the datePicker widget
    var datePicker = $("#datePicker").data("kendoDatePicker");
    // bind to the open event
    datePicker.bind("open", function(e) {
        // handle event
    });