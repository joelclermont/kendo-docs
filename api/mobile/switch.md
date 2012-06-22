---
title: kendo.mobile.ui.Switch
tags: api,mobile
publish: true
---

# kendo.mobile.ui.Switch

## Description



The mobile Switch widget is used to display two exclusive choices.

When initialized, it shows the currently selected value. User slides the control to reveal the second value.
The mobile Switch can be created from `input` element of type `checkbox`.

### Getting Started


<p> The Kendo Mobile Application will automatically initialize a mobile Switch for every element with `role` data attribute set to `swtich` present in the views/layouts markup.
Alternatively, it can be initialized using jQuery plugin syntax in the containing mobile View **init event handler**.

#### Initialize mobile Switch based on role data attribute

    <input type="checkbox" data-role="switch" />

#### Initialize mobile Switch using jQuery plugin syntax

    <input type="checkbox" id="switch" />
    <script>
    var switchWidget = $("#switch").kendoMobileSwitch();
    </script>

### Checking/Unchecking the Mobile Switch

The checked state of the mobile Switch depends on the `checked` property of the widget's constructor options
or the `checked` attribute of the widget's element.

#### Initialize Kendo mobile Switch from checked `input`

    <input type="checkbox" id="switch" checked="checked" />
    <script>
    var switchWidget = $("#switch").kendoMobileSwitch();
    </script>

#### Initialize checked mobile Switch using jQuery plugin syntax

    <input type="checkbox" id="switch" />
    <script>
    var switchWidget = $("#switch").kendoMobileSwitch({ checked: true });
    </script>

### Specifying the Text of the Labels

#### Customize Kendo mobile Switch on/off labels

    <input type="checkbox" id="switch" />
    <script>
    var switchWidget = $("#switch").kendoMobileSwitch({ onLabel: "YES", offLabel: "NO" });
    </script>

## Configuration

### `checked` : **Boolean** *(default: false)*

 The checked state of the widget.

### `offLabel` : **String** *(default: OFF)*

 The OFF label.

### `onLabel` : **String** *(default: ON)*

 The ON label.

## Methods

### check

Get/Set the checked state of the widget.

#### Example

    <input data-role="switch" id="foo" />;
    
    <script>
      // get a reference to the switch widget
      var switch = $("#foo").data("kendoMobileSwitch");
    
      // get the checked state of the switch.
      var checked = switch.check();
    
      // set the checked state of the switch.
      switch.check(true);
    </script>

#### Parameters

##### check `Boolean`

Whether to turn the widget on or off.

#### Returns

`Boolean` The checked state of the widget.

### toggle

Toggle the checked state of the widget.

#### Example

    <input data-role="switch" id="foo" />;
    
    <script>
      // get a reference to the switch
      var switch = $("#foo").data("kendoMobileSwitch");
    
      // toggle the checked state of the switch.
      switch.toggle();
    </script>

## Events

### change

Fires when the state of the widget changes

#### Handle mobile Switch change event

    <input type="checkbox" id="switch" data-role="switch" />
    
    <script>
     $("#switch").data("kendoMobileSwitch").bind("change", function(e) {
         console.log(e.checked); // true or false
     }
    </script>

#### Event Data

##### e.checked `Object`

The checked state of the widget.