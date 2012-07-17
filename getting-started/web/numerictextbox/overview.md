---
title: NumericTextBox Overview
slug: numerictextbox-overview
tags: getting-started,web
publish: true
---

# NumericTextBox Overview

The NumericTextBox widget can convert an INPUT element into a numeric, percentage or currency textbox.
The type is defined depending on the specified format. The widget renders spin buttons and with their help you can
increment/decrement the value with a predefined step. The NumericTextBox widget accepts only numeric entries.
The widget uses _kendo.culture.current_ culture in order to determine number precision and other culture
specific properties.


## Getting Started

### Creating a NumericTextBox from existing INPUT element

    <input id="textBox" />

### NumericTextBox initialization

    $(document).ready(function(){
        $("#textBox").kendoNumericTextBox();
    });

When a **NumericTextBox** is initialized, it will automatically
wraps the input element with span element and will render spin
buttons.

> When working the input being used for your NumericTextBox, always select by id instead of class. Behind the scenes, the NumericTextBox creates a secondary element to represent the visual look of the widget, and copies over all non-id attributes, including the class. As such, selecting this widget by class can cause unexpected results.

## Configuring NumericTextBox behaviors


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

### Customizing NumericTextBox defaults

     $("#textbox").kendoNumericTextBox({
         value: 10,
         min: -10,
         max: 100,
         step: 0.75,
         format: "n",
         decimals: 3
     });



### Create Currency NumericTextBox widget

     $("#textbox").kendoNumericTextBox({
         format: "c2" //Define currency type and 2 digits precision
     });



### Create Percentage NumericTextBox widget

     $("#textbox").kendoNumericTextBox({
         format: "p",
         value: 0.15 // 15 %
     });

## Accessing an Existing NumericTextBox


You can reference an existing **NumericTextBox** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the API to control
its behavior.

### Accessing an existing NumericTextBox instance

    var numericTextBox = $("#numericTextBox").data("kendoNumericTextBox");

