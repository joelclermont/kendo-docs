---
title: Globalization overview
slug: globalization-overview
publish: true
---
# Kendo Globalization Overview

Globalization is the process of designing and developing an application that works in multiple cultures. The culture defines specific information for the number formats, week and month names, date and time formats and etc.

Kendo provides a way to internationalize the current page using a culture script. Kendo exposes culture(cultureName) method which allows to select the culture script coresponding to the "`<language code>-<country/region code>`". For complete overview of the *culture* method, [review the Kendo API Reference](http://docs.kendoui.com/api/framework/kendo#culture).

## Define the current culture

First let's start by adding the required culture script:

### Add culture scripts to the page:

    <script src="jquery.js"></script>
    <script src="kendo.all.min.js"></script>
    <script src="kendo.culture.en-GB.js"></script>


Now, you just need to set the culture script, which kendo should use:

### Set current culture:

    <script type="text/javascript">
         //set current to the "en-GB" culture script
         kendo.culture("en-GB");
    </script>

The default culture, which Kendo widgets uses is "en-US".

## Format Number or Date object

Kendo exposes methods which can format number or date object using specific format string and the current specified culture:

- [kendo.toString(object, format)](http://docs.kendoui.com/api/framework/kendo#toString) - returns a string representation of the current object using specific format.
- [kendo.format(format, arguments)](http://docs.kendoui.com/api/framework/kendo#format) -  replaces each format item in a specified string with the text equivalent of a corresponding object's value.

For more detail information check [this help topic](http://docs.kendoui.com/getting-started/framework/globalization/formatting).

## Parsing a string
Kendo exposes methods which converts the specified string to date or number object:

- [kendo.parseInt(string, [culture])](http://docs.kendoui.com/api/framework/kendo#parseInt) - converts a string to a whole number using the specified culture (current culture by default).
- [kendo.parseFloat(string, [culture])](http://docs.kendoui.com/api/framework/kendo#parseFloat) - converts a string to a number with floating point using the specified culture (current culture by default).
- [kendo.parseDate(string, [formats], [culture])](http://docs.kendoui.com/api/framework/kendo#parseDate) - converts a string to a JavaScript Date object, taking into account the given format/formats (or the given culture's set of default formats).

For more detail information check [this help topic](http://docs.kendoui.com/getting-started/framework/globalization/parsers).

## Widgets that depend on culture info

Here is a list of widgets which depends on the current culture:

- Calendar
- DatePicker
- TimePicker
- DateTimePicker
- NumericTextBox
