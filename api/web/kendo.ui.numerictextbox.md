## Description


kendo.ui.NumericTextBox.Description

   The NumericTextBox widget can convert an INPUT element into a numeric, percentage or currency textbox.
   The type is defined depending on the specified format. The widget renders spin buttons and with their help you can
   increment/decrement the value with a predefined step. The NumericTextBox widget accepts only numeric entries.
   The widget uses _kendo.culture.current_ culture in order to determine number precision and other culture
   specific properties.


### Getting Started

#### Creating a NumericTextBox from existing INPUT element

    <input id="textBox" />


#### NumericTextBox initialization

    $(document).ready(function(){
     $("#textBox").kendoNumericTextBox();
    });


 When a **NumericTextBox** is initialized, it will automatically
 wraps the input element with span element and will render spin
 buttons.


### Configuring NumericTextBox behaviors


 The **NumericTextBox** provides configuration options that can be
 easily set during initialization. Among the properties that can be
 controlled:


*   Value of the **NumericTextBox**
*   Minimum and/or maximum values
*   Increment step
*   Precision of the number
*   Number format (any valid number format is allowed)



 To see a full list of available properties and values, review the
 Slider Configuration API documentation tab.

#### Customizing NumericTextBox defaults

     $("#textbox").kendoNumericTextBox({
         value: 10,
         min: -10,
         max: 100,
         step: 0.75,
         format: "n",
         decimals: 3
     });




#### Create Currency NumericTextBox widget

     $("#textbox").kendoNumericTextBox({
         format: "c2" //Define currency type and 2 digits precision
     });




#### Create Percentage NumericTextBox widget

     $("#textbox").kendoNumericTextBox({
         format: "p",
         value: 0.15 // 15 %
     });


### Accessing an Existing NumericTextBox


 You can reference an existing **NumericTextBox** instance via
 [jQuery.data()](http://api.jquery.com/jQuery.data/).
 Once a reference has been established, you can use the API to control
 its behavior.

#### Accessing an existing NumericTextBox instance

    var numericTextBox = $("#numericTextBox").data("kendoNumericTextBox");



------------------------------------------

## Configuration

### `decimals` : **Number** *(default: null)* 

 Specifies the number precision. If not set precision defined by current culture is used.

#### Example



    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 1,
        step: 0.1,
        decimals: 1
    });

### `downArrowText` : **String** *(default: Decrease value)* 

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

### `format` : **String** *(default: n)* 

 Specifies the format of the number. Any valid number format is allowed.

#### Example



    $("#numeric").kendoNumericTextBox({
       format: "p0", // format as percentage with % sign
       min: 0,
       max: 1,
       step: 0.01
    });

### `max` : **Number** *(default: null)* 

 Specifies the largest value the user can enter.

#### Example



    // specify in the HTML
    &lt;input id="numeric" value="10" type="number" min="-100" max="100" step="10"/&gt;
    <br />
    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50
    });

### `min` : **Number** *(default: null)* 

 Specifies the smallest value the user can enter.

#### Example



    // specify in the HTML
    &lt;input id="numeric" value="10" type="number" min="-100" max="100" step="10"/&gt;
    <br />
    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50
    });

### `placeholder` : **String** *(default: "")* 

 Specifies the text displayed when the input is empty.

#### Example



    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50,
        placeholder: "Select A Value"
    });

### `step` : **Number** *(default: 1)* 

 Specifies the increment/decrement step.

#### Example



    // specify in the HTML
    &lt;input id="numeric" value="10" type="number" /&gt;
    <br />
    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 1,
        step: 0.1
    });

### `upArrowText` : **String** *(default: Increase value)* 

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

### `value` : **Number** *(default: null)* 

 Specifies the value of the NumericTextBox widget.

#### Example



    // specify in the HTML
    &lt;input id="numeric" value="10" type="number" min="-100" max="100" step="10"/&gt;
    <br />
    // specify on widget initialization
    $("#numeric").kendoNumericTextBox({
        min: 0,
        max: 100,
        value: 50
    });



------------------------------------------

## Methods

### `enable`(enable)


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

### `value`(value)`Number`


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



------------------------------------------

## Events

### `change`
Fires when the value is changed

kendo.ui.NumericTextBox#change



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

### `spin`
Fires when the value is changed from the spin buttons

kendo.ui.NumericTextBox#spin



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

