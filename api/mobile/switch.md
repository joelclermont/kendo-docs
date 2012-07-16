---
title: kendo.mobile.ui.Switch
slug: mobile-kendo.mobile.ui.switch
tags: api,mobile
publish: true
---

# kendo.mobile.ui.Switch

## Configuration

### checked `Boolean`*(default: false)*

 The checked state of the widget.

### offLabel `String`*(default: OFF)*

 The OFF label.

### onLabel `String`*(default: ON)*

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
