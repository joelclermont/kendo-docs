---
title: kendo.ui.RangeSlider
slug: web-kendo.ui.rangeslider
tags: api,web
publish: true
---

# kendo.ui.RangeSlider

## Description

The **RangeSlider** widget display range of values and allows you to select ranges of values. Unlike the HTML5 range input, the **RangeSlider** presents a consistent experience across browsers and features a rich API and event model.

### Getting Started

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
scenarios where JavaScript is disabled, in which case users will be presented with two inputs, still allowing them to input a valid range.

### Customizing RangeSlider Behaviors

Many facets of the **RangeSlider** behavior can be configured through
properties, including:

*   Minimum and/or maximum values
*   Orientation (horizontal or vertical)
*   Small or large step
*   Tooltip format/placement

#### Initialize a RangeSlider and its properties

    $("#rangeSlider").kendoRangeSlider({
        min: 10,
        max: 50,
        orientation: "vertical",
        smallStep: 1,
        largeStep: 10
    });

### Accessing an Existing RangeSlider

You can reference an existing **RangeSlider** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

#### Accessing an existing RangeSlider instance

    var rangeSlider = $("#rangeSlider").data("kendoRangeSlider");

## Configuration

### largeStep `Number`*(default: 5)*

The delta with which the value will change when the user presses the Page Up or Page Down key (the drag
handle must be focused). Note: The allied largeStep will also set large tick for every large step.

### max `Number`*(default: 10)*

The maximum value of the **RangeSlider**.

### min `Number`*(default: 0)*

The minimum value of the **RangeSlider**.

### orientation `String`*(default: "horizontal")*

The orientation of a **RangeSlider**; **"horizontal"** or
**"vertical"**.

### selectionEnd `Number`

The selection end value of the **RangeSlider**.

### selectionStart `Number`

The selection start value of the **RangeSlider**.

### smallStep `Number`*(default: 1)*

The small step value of the **RangeSlider**. The underlying value will be changed when the end
user (1) clicks on the increase or decrease buttons of the **RangeSlider**, (2) presses the
arrow keys (the drag handle must be focused), or (3) drags the drag handle.

### tickPlacement `String`*(default: "both")*

Denotes the location of the tick marks in the **RangeSlider**. The available options are:


#### *"topLeft"*

Tick marks are located on the top of the horizontal widget or on the left of
  the vertical widget.

#### *"bottomRight"*

Tick marks are located on the bottom of the horizontal widget or on the
  right side of the vertical widget.

#### *"both"*

Tick marks are located on both sides of the widget.

#### *"none"*

Tick marks are not visible.

### tooltip `Object`

Configuration of the **RangeSlider** tooltip.

### tooltip.enabled `Boolean`*(default: true)*

Disables (**false**) or enables (**true**) the tooltip of the **RangeSlider**.

### tooltip.format `String`*(default: "{0}")*

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