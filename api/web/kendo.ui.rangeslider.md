

------------------------------------------

## Configuration

### `largeStep` : **Number** *(default: 5)* 

The delta with which the value will change when the user presses the Page Up or Page Down key (the draghandle must be focused). Note: The allied largeStep will also set large tick for every large step.

### `max` : **Number** *(default: 10)* 

The maximum value of the <strong>RangeSlider</strong>.

### `min` : **Number** *(default: 0)* 

The minimum value of the <strong>RangeSlider</strong>.

### `orientation` : **String** *(default: "horizontal")* 

The orientation of a <strong>RangeSlider</strong>; <strong>"horizontal"</strong> or<strong>"vertical"</strong>.

### `selectionEnd` : **Number** *(default: 10)* 

The selection end value of the <strong>RangeSlider</strong>.

### `selectionStart` : **Number** *(default: 0)* 

The selection start value of the <strong>RangeSlider</strong>.

### `smallStep` : **Number** *(default: 1)* 

The small step value of the <strong>RangeSlider</strong>. The underlying value will be changed when the enduser (1) clicks on the increase or decrease buttons of the <strong>RangeSlider</strong>, (2) presses thearrow keys (the drag handle must be focused), or (3) drags the drag handle.

### `tickPlacement` : **String** *(default: "both")* 

Denotes the location of the tick marks in the <strong>RangeSlider</strong>. The available options are:<div class="details-list">   <dl>        <dt>             <code>"topLeft"</code>        </dt>        <dd>             Tick marks are located on the top of the horizontal widget or on the left of  the vertical widget.        </dd>        <dt>             <code>"bottomRight"</code>        </dt>        <dd>            Tick marks are located on the bottom of the horizontal widget or on the  right side of the vertical widget.        </dd>        <dt>             <code>"both"</code>        </dt>        <dd>            Tick marks are located on both sides of the widget.        </dd>        <dt>             <code>"none"</code>        </dt>        <dd>            Tick marks are not visible.        </dd>   </dl></div>

### `tooltip` : **Object**  

Configuration of the <strong>RangeSlider</strong> tooltip.

### `tooltip.enabled` : **Boolean** *(default: true)* 

Disables (<b>false</b>) or enables (<b>true</b>) the tooltip of the <strong>RangeSlider</strong>.

### `tooltip.format` : **String** *(default: "{0}")* 

Format string for the text of the tooltip. Note: The applied format will also influence the appearance ofthe <strong>RangeSlider</strong> tick labels.



------------------------------------------

## Methods

### `enable`(enable)


Enable/Disable the **RangeSlider** widget.

#### Example

    // get a reference to the range slider widget
    var rangeSlider = $("#rangeSlider").data("kendoRangeSlider");
    
    // disables the range slider
    rangeSlider.enable(false);
    
    // enables the range slider
    rangeSlider.enable(true);

#### Parameters 

##### enable `Boolean`

The argument, which defines whether to enable/disable the **RangeSlider**.

### `value`(value)


The value method gets or sets the start and end values of the **RangeSlider**. It
accepts an array as parameter, and returns an object array with the start and end
selection values.

#### Example

    var rangeSider = $("#rangeSlider").data("kendoRangeSlider");
    rangeSlider.value();

#### Parameters 

##### value ``





------------------------------------------

## Events

### `change`
Fires when the rangeSlider value changes as a result of selecting a new value with one of the drag handles or the keyboard.

kendo.ui.RangeSlider#change


#### Event Data 

##### e.value `Number`

Represents the updated array of values of the first and second drag handle.

### `slide`
Fires when the user drags the drag handle to a new position.

kendo.ui.RangeSlider#slide


#### Event Data 

##### e.value `Number`

Represents an array of values of the current positions of the first and second drag handle.

