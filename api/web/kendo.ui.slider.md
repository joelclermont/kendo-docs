## Description


kendo.ui.Slider.Description

 The **Slider** provides a rich input for selecting values or ranges of values. Unlike the HTML5
 range input, the **Slider** presents a consistent experience across browsers and features a rich
 API and event model.


### Getting Started

There are two types of **Slider**:

1.  **Slider**, which presents one thumb and two opposing buttons for selecting a single value
2.  **RangeSlider**, which present two thumbs for defining a range of values


#### Slider

#### Create an input element

    <input id="slider" />


 Initialization of a **Slider** should occur after the DOM is fully loaded. It is recommended that
 initialization the **Slider** occur within a handler is provided to $(document).ready().

#### Initialize a Slider using a selector within $(document).ready()

    $(document).ready(function() {
        $("#slider").kendoSlider();
    });


#### RangeSlider

#### Create two HTML input elements in a div

    <div id="rangeSlider">
        <input />
        <input />
    </div>


 Initialization of a **RangeSlider** should occur after the DOM is fully loaded. It is recommended
 that initialization the **RangeSlider** occur within a handler is provided to $(document).ready().

#### Initialize a RangeSlider using a selector within $(document).ready()

    $(document).ready(function() {
        $("#rangeSlider").kendoRangeSlider();
    });


 The **RangeSlider** requires two inputs to capture both ends of the value range. This benefits
 scenarios where JavaScript is disabled, in which case users will be presented with two inputs, still allowing
 them to input a valid range.


### Customizing Slider Behaviors


 Many facets of the **Slider** and **RangeSlider** behavior can be configured through
 properties, including:


*   Minimum and/or maximum values
*   Orientation (horizontal or vertical)
*   Small or large step
*   Tooltip format/placement

#### Initialize a Slider and its properties

    $("#slider").kendoSlider({
        min: 10,
        max: 50,
        orientation: "vertical",
        smallStep: 1,
        largeStep: 10
    });


### Accessing an Existing Slider


 You can reference an existing **Slider** instance via
 [jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
 use the API to control its behavior.

#### Accessing an existing Slider instance

    var slider = $("#slider").data("kendoSlider");



------------------------------------------

## Configuration

### `decreaseButtonTitle` : **String** *(default: "Decrease")* 

The title of the decrease button of the <strong>Slider</strong>.

### `increaseButtonTitle` : **String** *(default: "Increase")* 

The title of the increase button of the <strong>Slider</strong>.

### `largeStep` : **Number** *(default: 5)* 

The delta with which the value will change when the user presses the Page Up or Page Down key (the draghandle must be focused). Note: The allied largeStep will also set large tick for every large step.

### `max` : **Number** *(default: 10)* 

The maximum value of the <strong>Slider</strong>.

### `min` : **Number** *(default: 0)* 

The minimum value of the <strong>Slider</strong>.

### `orientation` : **String** *(default: "horizontal")* 

The orientation of a <strong>Slider</strong>; <strong>"horizontal"</strong> or <strong>"vertical"</strong>.

### `showButtons` : **Boolean** *(default: true)* 

Can be used to show (<b>true</b>) or hide (<b>false</b>) theincrease and decrease buttons of a <strong>Slider</strong>.

### `smallStep` : **Number** *(default: 1)* 

The small step value of the <strong>Slider</strong>. The underlying value will be changed when the end user(1) clicks on the increase or decrease buttons of the <strong>Slider</strong>, (2) presses the arrow keys(the drag handle must be focused), or (3) drags the drag handle.

### `tickPlacement` : **String** *(default: "both")* 

Denotes the location of the tick marks in the <strong>Slider</strong>. The available options are:<div class="details-list">   <dl>        <dt>             <code>"topLeft"</code>        </dt>        <dd>             Tick marks are located on the top of the horizontal widget or on the left of  the vertical widget.        </dd>        <dt>             <code>"bottomRight"</code>        </dt>        <dd>            Tick marks are located on the bottom of the horizontal widget or on the  right side of the vertical widget.        </dd>        <dt>             <code>"both"</code>        </dt>        <dd>            Tick marks are located on both sides of the widget.        </dd>        <dt>             <code>"none"</code>        </dt>        <dd>            Tick marks are not visible.        </dd>   </dl></div>

### `tooltip` : **Object**  

Configuration of the <strong>Slider</strong> tooltip.

### `tooltip.enabled` : **Boolean** *(default: true)* 

Disables (<b>false</b>) or enables (<b>true</b>) the tooltip ofthe <strong>Slider</strong>.

### `tooltip.format` : **String** *(default: "{0}")* 

Format string for the text of the tooltip. Note: The appliedformat will also influence the appearance of the <strong>Slider</strong>tick labels.

### `value` : **Number** *(default: 0)* 

The underlying value of the <strong>Slider</strong>.



------------------------------------------

## Methods

### `enable`(enable)


Enable/Disable the **Slider** widget.

#### Example

    // get a reference to the slider widget
    var slider = $("#slider").data("kendoSlider");
    
    // disables the slider
    slider.enable(false);
    
    // enables the slider
    slider.enable(true);

#### Parameters 

##### enable `Boolean`

The argument, which defines whether to enable/disable the **Slider**.

### `value`(value)


Gets or sets the value of a **Slider**. It accepts a string or number as parameters and returns
a number representing the underlying value.

#### Example

    var slider = $("#slider").data("kendoSlider");
    var sliderValue = slider.value();

#### Parameters 

##### value `String`

_optional, default: _

The value to be set for a Slider.



------------------------------------------

## Events

### `change`
Fires when the slider value changes as a result of selecting a new value with the drag handle, buttons or keyboard.

kendo.ui.Slider#change


#### Event Data 

##### e.value `Number`

Represents the updated value of the slider.

### `slide`
Fires when the user drags the drag handle to a new position.

kendo.ui.Slider#slide


#### Event Data 

##### e.value `Number`

Represents the value from the current position of the drag handle.

