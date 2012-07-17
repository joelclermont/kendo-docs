---
title: kendo.ui.NumericTextBox
slug: web-kendo.ui.numerictextbox
tags: api,web
publish: true
---

# kendo.ui.NumericTextBox

## Configuration

### culture `String`*(default: en-US)*

 Specifies the culture info used by the NumericTextBox widget.

#### Example

    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        culture: "de-DE"
    });

### decimals `Number`*(default: null)*

 Specifies the number precision. If not set precision defined by current culture is used.

#### Example

    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 1,
        step: 0.1,
        decimals: 1
    });

### downArrowText `String`*(default: Decrease value)*

 Specifies the text of the tooltip on the down arrow.

#### Example

    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50,
        upArrowText: "More",
        downArrowText: "Less"
    });

### format `String`*(default: n)*

 Specifies the format of the number. Any valid number format is allowed.

#### Example

    $("#numeric").kendoNumericTextBox({
       format: "p0", // format as percentage with % sign
       min: 0,
       max: 1,
       step: 0.01
    });

### max `Number`*(default: null)*

 Specifies the largest value the user can enter.

#### Example

    // specify in the HTML
    <input id="numeric" value="10" type="number" min="-100" max="100" step="10"/>
    <br />
    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50
    });

### min `Number`*(default: null)*

 Specifies the smallest value the user can enter.

#### Example

    // specify in the HTML
    <input id="numeric" value="10" type="number" min="-100" max="100" step="10"/>
    <br />
    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50
    });

### placeholder `String`*(default: "")*

 Specifies the text displayed when the input is empty.

#### Example

    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50,
        placeholder: "Select A Value"
    });

### step `Number`*(default: 1)*

 Specifies the increment/decrement step.

#### Example

    // specify in the HTML
    <input id="numeric" value="10" type="number" />
    <br />
    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 1,
        step: 0.1
    });

### upArrowText `String`*(default: Increase value)*

 Specifies the text of the tooltip on the up arrow.

#### Example

    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50,
        upArrowText: "More",
        downArrowText: "Less"
    });

### value `Number`*(default: null)*

 Specifies the value of the NumericTextBox widget.

#### Example

    // specify in the HTML
    <input id="numeric" value="10" type="number" min="-100" max="100" step="10"/>
    
    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50
    });

## Methods

### enable

Enable/Disable the numerictextbox widget.

#### Example

    // get a reference to the numeric textbox
    var textbox = $("#textbox").data("kendoNumericTextBox");
    
    // disables the numerictextbox
    numerictextbox.enable(false);
    
    // enables the numerictextbox
    numerictextbox.enable(true);

#### Parameters

##### enable `Boolean`

The argument, which defines whether to enable/disable tha numerictextbox.

### max

Gets/Sets the max value of the NumericTextBox.

#### Example

    // get a reference to the NumericTextBox widget
    var numerictextbox = $("#numerictextbox").data("kendoNumericTextBox");
    
    // get the max value of the numerictextbox.
    var max = numerictextbox.max();
    
    // set the max value of the numerictextbox.
    numerictextbox.max(10);

#### Parameters

##### value `Number | String`

The max value to set.

#### Returns

`Number` The max value of the NumericTextBox.

### min

Gets/Sets the min value of the NumericTextBox.

#### Example

    // get a reference to the NumericTextBox widget
    var numerictextbox = $("#numerictextbox").data("kendoNumericTextBox");
    
    // get the min value of the numerictextbox.
    var min = numerictextbox.min();
    
    // set the min value of the numerictextbox.
    numerictextbox.min(-10);

#### Parameters

##### value `Number | String`

The min value to set.

#### Returns

`Number` The min value of the NumericTextBox.

### step

Gets/Sets the step value of the NumericTextBox.

#### Example

    // get a reference to the NumericTextBox widget
    var numerictextbox = $("#numerictextbox").data("kendoNumericTextBox");
    
    // get the step value of the numerictextbox.
    var step = numerictextbox.step();
    
    // set the step value of the numerictextbox.
    numerictextbox.step(0.1);

#### Parameters

##### value `Number | String`

The step value to set.

#### Returns

`Number` The step value of the NumericTextBox.

### value

Gets/Sets the value of the numerictextbox.

#### Example

    // get a referene to the numeric textbox
    var numerictextbox = $("#textbox").data("kendoNumericTextBox");
    
    // get the value of the numerictextbox.
    var value = numerictextbox.value();
    
    // set the value of the numerictextbox.
    numerictextbox.value("10.20");

#### Parameters

##### value `Number | String`

The value to set.

#### Returns

`Number` The value of the numerictextbox.

## Events

### change

Fires when the value is changed

#### Example

    $("#numeric").kendoNumericTextBox({
        change: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the numeric textbox widget
    var numeric = $("#numeric").data("kendoNumericTextBox");
    // bind to the change event
    numeric.bind("change", function(e) {
        // handle event
    });

### spin

Fires when the value is changed from the spin buttons

#### Example

    $("#numeric").kendoNumericTextBox({
        spin: function(e) {
            // handle event
        }
    });

#### To set after initialization

    // get a reference to the numeric textbox widget
    var numeric = $("#numeric").data("kendoNumericTextBox");
    // bind to the spin event
    numeric.bind("spin", function(e) {
        // handle event
    });
