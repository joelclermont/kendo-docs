# kendo.ui.RangeSlider

## Configuration

### `largeStep` : **Number** *(default: 5)*

The delta with which the value will change when the user presses the Page Up or Page Down key (the drag
handle must be focused). Note: The allied largeStep will also set large tick for every large step.

### `max` : **Number** *(default: 10)*

The maximum value of the **RangeSlider**.

### `min` : **Number** *(default: 0)*

The minimum value of the **RangeSlider**.

### `orientation` : **String** *(default: "horizontal")*

The orientation of a **RangeSlider**; **"horizontal"** or
**"vertical"**.

### `selectionEnd` : **Number** *(default: 10)*

The selection end value of the **RangeSlider**.

### `selectionStart` : **Number** *(default: 0)*

The selection start value of the **RangeSlider**.

### `smallStep` : **Number** *(default: 1)*

The small step value of the **RangeSlider**. The underlying value will be changed when the end
user (1) clicks on the increase or decrease buttons of the **RangeSlider**, (2) presses the
arrow keys (the drag handle must be focused), or (3) drags the drag handle.

### `tickPlacement` : **String** *(default: "both")*

Denotes the location of the tick marks in the **RangeSlider**. The available options are:
<div class="details-list">
   <dl>
        <dt>
             `"topLeft"`
        </dt>
        <dd>
             Tick marks are located on the top of the horizontal widget or on the left of
  the vertical widget.
        </dd>
        <dt>
             `"bottomRight"`
        </dt>
        <dd>
            Tick marks are located on the bottom of the horizontal widget or on the
  right side of the vertical widget.
        </dd>
        <dt>
             `"both"`
        </dt>
        <dd>
            Tick marks are located on both sides of the widget.
        </dd>
        <dt>
             `"none"`
        </dt>
        <dd>
            Tick marks are not visible.
        </dd>
   </dl>
</div>

### `tooltip` : **Object** 

Configuration of the **RangeSlider** tooltip.

### `tooltip.enabled` : **Boolean** *(default: true)*

Disables (**false**) or enables (**true**) the tooltip of the **RangeSlider**.

### `tooltip.format` : **String** *(default: "{0}")*

Format string for the text of the tooltip. Note: The applied format will also influence the appearance of
the **RangeSlider** tick labels.

## Methods

### enable

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

### value

The value method gets or sets the start and end values of the **RangeSlider**. It
accepts an array as parameter, and returns an object array with the start and end
selection values.

#### Example

    var rangeSider = $("#rangeSlider").data("kendoRangeSlider");
    rangeSlider.value();

#### Parameters

##### value ``



## Events

### change

Fires when the rangeSlider value changes as a result of selecting a new value with one of the drag handles or the keyboard.

#### Event Data

##### e.value `Number`

Represents the updated array of values of the first and second drag handle.

### slide

Fires when the user drags the drag handle to a new position.

#### Event Data

##### e.value `Number`

Represents an array of values of the current positions of the first and second drag handle.