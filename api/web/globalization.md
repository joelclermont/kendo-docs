---title: kendo.ui.Globalization
tags: api,web
publish: true
---
# kendo.ui.Globalization

## Description



Globalization is the process of designing and developing an
application that works in multiple cultures. The culture defines specific information
for the number formats, week and month names, date and time formats and etc.

Kendo exposes **_culture(cultureName)_** method which allows to select the culture
script corresponding to the "culture name". kendo.culture() method uses the passed culture name
to select a culture from the culture scripts that you have included and then sets the current culture. If there is no
corresponding culture then the method will try to find culture which is equal to the country part of the culture name.
If no culture is found the default one is used.



### Define current culture settings

#### Include culture scripts and select culture

    
    <script src="jquery.js" ></script>
    <script src="kendo.all.min.js"></script>
    <script src="kendo.culture.en-GB.js"></script>
    <script type="text/javascript">
       //set current culture to the "en-GB" culture script.
       kendo.culture("en-GB");
    </script>

#### Select closest culture

    
    <script src="jquery.js" ></script>
    <script src="kendo.all.min.js"></script>
    <script src="kendo.culture.fr.js"></script>
    <script type="text/javascript">
       //set current culture to the "fr" culture script.
       kendo.culture("fr-FR");
    </script>

#### Get current culture

    var cultureInfo = kendo.culture();
    
    <h3>Find culture object</h3>

Kendo also exposes **_findCulture(cultureName)_** method which returns a culture object which corresponds to
the passed culture name. If there is no such culture in the registered culture scripts, the method will try to find a culture object
which corresponds to the country part of the culture name. If no culture is found, the result will be **null**.

#### Find a culture object

    
    <script src="jquery.js" ></script>
    <script src="kendo.all.min.js"></script>
    <script src="kendo.culture.fr.js"></script>
    <script type="text/javascript">
       //finds the "fr-FR" culture object.
       var culture = kendo.findCulture("fr-FR");
    </script>

### Format number or date object


Kendo exposes methods which can format number or date object using specific format string and the current specified culture:

#### `kendo.toString(object, format)` - returns a string representation of the current object using specific format.

#### Formats number and date objects

    //format number using standard number format
    kendo.toString(10.12, "n"); //10.12
    kendo.toString(10.12, "n0"); //10
    kendo.toString(10.12, "n5"); //10.12000
    kendo.toString(10.12, "c"); //$10.12
    kendo.toString(0.12, "p"); //12.00 %
    //format number using custom number format
    kendo.toString(19.12, "00##"); //0019
    //format date
    kendo.toString(new Date(2010, 9, 5), "yyyy/MM/dd" ); // "2010/10/05"
    kendo.toString(new Date(2010, 9, 5), "dddd MMMM d, yyyy" ); // "Tuesday October 5, 2010"
    kendo.toString(new Date(2010, 10, 10, 22, 12), "hh:mm tt" ); // "10:12 PM"

#### kendo.format - replaces each format item in a specified string with the text equivalent of a corresponding object's value.

#### String format

     kendo.format("{0} - {1}", 12, 24); //12 - 24
     kendo.format("{0:c} - {1:c}", 12, 24); //$12.00 - $24.00

### Parsing a string


Kendo exposes methods which converts the specified string to date or number object:
<ol>
   <li>
      `kendo.parseInt(string, [culture])` - converts a string to a whole number using the specified culture (current culture by default).

#### Parse string to integer

    
           //assumes that current culture defines decimal separator as "."
           kendo.parseInt("12.22"); //12
    
           //assumes that current culture defines decimal separator as ",", group separator as "." and currency symbol as "€"
           kendo.parseInt("1.212,22 €"); //1212
       </li>
       <li>
          <code>kendo.parseFloat(string, [culture])</code> - converts a string to a number with floating point using the specified culture (current culture by default).

#### Parse string to float

    
           //assumes that current culture defines decimal separator as "."
           kendo.parseFloat("12.22"); //12.22
    
           //assumes that current culture defines decimal separator as ",", group separator as "." and currency symbol as "€"
           kendo.parseFloat("1.212,22 €"); //1212.22
       </li>
       <li>
          <code>kendo.parseDate(string, [formats], [culture])</code> - converts a string to a JavaScript Date object, taking into account the given format/formats (or the given culture's set of default formats).
          Current culture is used if one is not specified.

#### Parse string to float

    
           //current culture is "en-US"
           kendo.parseDate("12/22/2000"); //Fri Dec 22 2000
           kendo.parseDate("2000/12/22", "yyyy/MM/dd"); //Fri Dec 22 2000
       </li>
    </ol>

### Number formatting

The purpose of number formatting is to convert Number object to a human readable string using culture's specific settings. `kendo.format` and `kendo.toString`
methods support standard and custom numeric formats:


#### Standard numeric formats

**n** for number

#### Formatting using "n" format

          kendo.culture("en-US");
          kendo.toString(1234.567, "n"); //1,234.57
    
          kendo.culture("de-DE");
          kendo.toString(1234.567, "n3"); //1.234,567

**c** for currency

#### Formatting using "c" format

          kendo.culture("en-US");
          kendo.toString(1234.567, "c"); //$1,234.57
    
          kendo.culture("de-DE");
          kendo.toString(1234.567, "c3"); //1.234,567 €

**p** for percentage (number is multiplied by 100)

#### Formatting using "p" format

          kendo.culture("en-US");
          kendo.toString(0.222, "p"); //22.20 %
    
          kendo.culture("de-DE");
          kendo.toString(0.22, "p3"); //22.000 %

**e** for exponential

#### Formatting using "e" format

          kendo.toString(0.122, "e"); //1.22e-1
          kendo.toString(0.122, "e4"); //1.2200e-1

#### Custom numeric formats

You can create custom numeric format string using one or more custom numeric specifiers. Custom numeric format string is any tha is not a standard numeric format.
<div class="details-list">
  

#### Format specifiers

  <dl>
    <dt>
      "0" - zero placeholder
    </dt>
    <dd>Replaces the zero with the corresponding digit if one is present; otherwise, zero appears in the result string - `kendo.toString(1234.5678, "00000") -> 01235`</dd>
    <dt>
      "#" - digit placeholder
    </dt>
    <dd>Replaces the pound sign with the corresponding digit if one is present; otherwise, no digit appears in the result string - `kendo.toString(1234.5678, "#####") -> 1235`</dd>
    <dt>
      "." - Decimal placeholder
    </dt>
    <dd>Determines the location of the decimal separator in the result string - `kendo.tostring(0.45678, "0.00") -> 0.46 `(en-us)</dd>
    <dt>
      "," - group separator placeholder
    </dt>
    <dd>Insert localized group separator between each group - `kendo.tostring(12345678, "##,#") -> 12,345,678`(en-us)</dd>
    <dt>
      "%" - percentage placeholder
    </dt>
    <dd>Multiplies a number by 100 and inserts a localized percentage symbol in the result string</dd>
    <dt>
      "e" - exponential notation
    </dt>
    <dd>`kendo.toString(0.45678, "e0") -> 5e-1`</dd>
    <dt>
      ";" - section separator
    </dt>
    <dd>Defines sections wih separate format strings for positive, negative, and zero numbers</dd>
    <dt>
      "string"/'string' - Literal string delimiter
    </dt>
    <dd>Indicates that the enclosed characters should be copied to the result string</dd>
  </dl>
</div>

### Date formatting

The purpose of date formatting is to convert Date object to a human readable string using culture's specific settings. `kendo.format` and `kendo.toString`
methods support standard and custom date formats:


#### Standard date formats

<div class="details-list">
  

#### Format specifiers

  <dl>
    <dt>
      "d" - short date pattern
    </dt>
    <dd>`kendo.toString(new Date(2000, 10, 6), "d") -> 11/6/2000`</dd>
    <dt>
      "D" - long date pattern
    </dt>
    <dd>`kendo.toString(new Date(2000, 10, 6), "D") -> Monday, November 06, 2000`</dd>
    <dt>
      "F" - Full date/time pattern
    </dt>
    <dd>`kendo.toString(new Date(2000, 10, 6), "D") -> Monday, November 06, 2000 12:00:00 AM`</dd>
    <dt>
      "g" - General date/time pattern (short time)
    </dt>
    <dd>`kendo.toString(new Date(2000, 10, 6), "g") -> 11/6/2000 12:00 AM`</dd>
    <dt>
      "G" - General date/time pattern (long time)
    </dt>
    <dd>`kendo.toString(new Date(2000, 10, 6), "G") -> 11/6/2000 12:00:00 AM`</dd>
    <dt>
      "M/m" - Month/day pattern
    </dt>
    <dd>`kendo.toString(new Date(2000, 10, 6), "m") -> November 06`</dd>
    <dt>
      "u" - Universal sortable date/time pattern
    </dt>
    <dd>`kendo.toString(new Date(2000, 10, 6), "u") -> 2000-11-06 00:00:00Z`</dd>
    <dt>
      "Y/y" - Year/month pattern
    </dt>
    <dd>`kendo.toString(new Date(2000, 10, 6), "y") -> November, 2000`</dd>
  </dl>
</div>

#### Custom date formats

<div class="details-list">
  

#### Format specifiers

  <dl>
    <dt>
      "d"
    </dt>
    <dd>The day of the month, from 1 through 31</dd>
    <dt>
      "dd"
    </dt>
    <dd>The day of the month, from 01 through 31.</dd>
    <dt>
      "ddd"
    </dt>
    <dd>iThe abbreviated name of the day of the week</dd>
    <dt>
      "dddd"
    </dt>
    <dd>The full name of the day of the week</dd>
    <dt>
      "f"
    </dt>
    <dd>The tenths of a second in a date and time value</dd>
    <dt>
      "ff"
    </dt>
    <dd>The hundredths of a second in a date and time value</dd>
    <dt>
      "fff"
    </dt>
    <dd>The milliseconds in a date and time value</dd>
    <dt>
      "M"
    </dt>
    <dd>The month, from 1 through 12</dd>
    <dt>
      "MM"
    </dt>
    <dd>The month, from 01 through 12</dd>
    <dt>
      "MMM"
    </dt>
    <dd>The abbreviated name of the month</dd>
    <dt>
      "MMMM"
    </dt>
    <dd>The full name of the month</dd>
    <dt>
      "h"
    </dt>
    <dd>The hour, using a 12-hour clock from 1 to 12</dd>
    <dt>
      "hh"
    </dt>
    <dd>The hour, using a 12-hour clock from 01 to 12</dd>
    <dt>
      "H"
    </dt>
    <dd>The hour, using a 24-hour clock from 1 to 23</dd>
    <dt>
      "HH"
    </dt>
    <dd>The hour, using a 24-hour clock from 01 to 23</dd>
    <dt>
      "m"
    </dt>
    <dd>The minute, from 0 through 59</dd>
    <dt>
      "mm"
    </dt>
    <dd>The minute, from 00 through 59</dd>
    <dt>
      "s"
    </dt>
    <dd>The second, from 0 through 59</dd>
    <dt>
      "ss"
    </dt>
    <dd>The second, from 00 through 59</dd>
    <dt>
      "tt"
    </dt>
    <dd>The AM/PM designator</dd>
  </dl>
</div>

### Widgets that depend on current culture are:

*   Calendar*   DatePicker*   TimePicker*   NumericTextBox

## Configuration

## Methods

## Events