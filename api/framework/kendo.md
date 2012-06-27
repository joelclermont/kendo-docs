---
title: kendo
tags: api,framework
publish: true
---

# kendo

## Methods

### bind
Binds a HTML View to a View-Model.

Model View ViewModel ([MVVM](http://en.wikipedia.org/wiki/Model_View_ViewModel)) is a design pattern which helps developers separate the Model from the View. The View-Model part of MVVM is responsible for
exposing the data objects from the Model in such a way that those objects are easily consumed in the View.

#### Example
     <!-- View -->
     <div id="view">
       <!-- The value of the INPUT element is bound to the "firstName" field of the View-Model.
       When the value changes so will the "firstName" field and vice versa.  -->
       <label>First Name:<input data-bind="value: firstName" /></label>
       <!-- The value of the INPUT element is bound to the "lastName" field of the View-Model.
       When the value changes so will the "lastName" field and vice versa.   -->
       <label>Last Name:<input data-bind="value: lastName" /></label>
       <!-- The click event of the BUTTON element is bound to the "displayGreeting" method of the View-Model.
       When the user clicks the button the "displayGreeting" method will be invoked.  -->
       <button data-bind="click: displayGreeting">Display Greeting</button>
     </div>
     <script>
       // View-Model
       var viewModel = kendo.observable({
          firstName: "John",
          lastName: "Doe",
          displayGreeting: function() {
              // Get the current values of "firstName" and "lastName"
              var firstName = this.get("firstName");
              var lastName = this.get("lastName");
              alert("Hello, " + firstName + " " + lastName + "!!!");
          }
       });

       // Bind the View to the View-Model
       kendo.bind($("#view"), viewModel);
     </script>
#### Parameters

##### element `String|jQuery|Node`

The root element(s) from which the binding starts. Can be a valid jQuery string selector, a DOM element or a jQuery object.
All child elements are traversed.

##### viewModel `Object|kendo.data.ObservableObject`

The View-Model which the elements are bound to. Wraped as an instance of `kendo.data.ObservableObject` if not already.

##### namespace `Object`

Optional namespace(s) too look in when instantiating Kendo UI widgets. The valid namespaces are `kendo.ui`, `kendo.dataviz.ui` and `kendo.mobile.ui`. The default
order is `kendo.ui`, `kendo.dataviz.ui`.

### culture
Sets or gets the current culture. Uses the passed culture name to select a culture from the culture scripts that you have included and then sets the current culture.
If there is no corresponding culture then the method will try to find culture which is equal to the country part of the culture name.
If no culture is found the default one is used.

#### Include culture JavaScript files and select a culture
    <script src="jquery.js" ></script>
    <script src="kendo.all.min.js"></script>
    <script src="kendo.culture.en-GB.js"></script>
    <script>
    //set current culture to "en-GB".
    kendo.culture("en-GB");
    </script>
#### Get the current culture
    var culture = kendo.culture();

### format
Replaces each format item in a specified string with the text equivalent of a corresponding object's value.

#### Example
    kendo.format("{0} - {1}", 12, 24); //12 - 24
    kendo.format("{0:c} - {1:c}", 12, 24); //$12.00 - $24.00

#### Returns

`String` The formatted string.

### htmlEncode

Encodes HTML characters to entities.

#### Example
    var html = kendo.htmlEncode("<span>Hello</span>");
    console.log(html); // outputs "&lt;span&gt;Hello&lt;/span&gt;"

#### Parameters

##### value `String`

The string that needs to be HTML encoded.

#### Returns

`String` The encoded string.

### parseDate
Parses as a formatted string as a `Date`.
#### Example
    kendo.parseDate("12/22/2000"); //Fri Dec 22 2000
    kendo.parseDate("2000/12/22", "yyyy/MM/dd"); //Fri Dec 22 2000
#### Returns
`Date` the parsed date.

#### Parameters

##### value `String`
The formatted string which should be parsed as date.

##### formats `String|Array` *(optional)*
The format(s) that will be used to parse the date. By default all standard date formats are used.

##### culture `String` *(optional)*
The culture used to parse the number. The current culture is used by default.

### parseFloat
Parses as a formatted string as a floating point number.

#### Example
    kendo.parseFloat("12.22"); //12.22

    kendo.culture("de-DE");
    kendo.parseFloat("1.212,22 €"); //1212.22
#### Returns
`Number` the parsed number.

#### Parameters

##### value `String`
The formatted string which should be parsed as number.

##### culture `String` *(optional)*
The culture used to parse the number. The current culture is used by default.

### parseInt
Parses as a formatted string as an integer.
#### Example
    kendo.parseInt("12.22"); //12

    kendo.culture("de-DE");
    kendo.parseInt("1.212,22 €"); //1212
#### Returns
`Number` the parsed number.

#### Parameters

##### value `String`
The formatted string which should be parsed as number.

##### culture `String` *(optional)*
The culture used to parse the number. The current culture is used by default.

### render

Renders the specified template using the provided data.

#### Example
    var template = kendo.template("<li>#: name #</li>");
    var data = [ { name: "John Doe" }, { name: "Jane Doe" }];
    $("ul").html(kendo.render(template, data)); // sets the html to <li>John Doe</li><li>Jane Doe</li>

#### Parameters

##### template `Function`

The Kendo template which should be rendered.

##### data `Array`

Array of JavaScript objects which contains the data that the template will render.

### template
Compiles a template to a function that builds HTML. Useful when a template will be used several times.
Templates offer way of creating HTML chunks. Options such as HTML encoding and compilation for optimal
performance are available.

#### Returns
`Function` the compiled template as a JavaScript function. When called this function will return the generated HTML string.

#### Basic template

    var inlineTemplate = kendo.template("Hello, #= firstName # #= lastName #");
    var inlineData = { firstName: "John", lastName: "Doe" };
    $("#inline").html(inlineTemplate(inlineData));

#### Output:

    Hello, John Doe!

#### Encode HTML

    var encodingTemplate = kendo.template("HTML tags are encoded as follows: #:html#");
    var encodingData = { html: "<strong>lorem ipsum</strong>" };
    $("#encoding").html(encodingTemplate(encodingData));

#### Output:

    HTML tags are encoded as follows: <strong>lorem ipsum</strong>

#### Use JavaScript in templates

    var encodingTemplate = kendo.template("#if (foo) {# bar #}#");
    var data = { foo: true};
    $("#encoding").html(encodingTemplate(data)); // outputs bar

#### Escape sharp symbols in JavaScript strings

    var encodingTemplate = kendo.template("<a href='\\#'>Link</a>");

#### Escape sharp symbols in script templates

    <script type="text/x-kendo-template" id="template">
     <a href="\#">Link</a>
    </script>

    <script>
    var encodingTemplate = kendo.template($("#template").html());
    </script>

#### Parameters
##### template `String`

The template that will be compiled.
##### options `Object` (optional)
Template compilation options.

##### options.paramName `String` *(default: "data")*
The name of the parameter used by the generated function. Useful when `useWithBlock` is set to `false`.

###### Example
    var template = kendo.template("<strong>#: d.name #</strong>", { paramName: "d", useWithBlock: false });

##### options.useWithBlock `Boolean` *(default: true)*
Wraps the generated code in a `with` block. This allows the usage of unqualified fields in the template. Disabling the `with` block will improve
the performance of the template.

###### Example
    var template = kendo.template("<strong>#: data.name #</strong>", { useWithBlock: false }); // Note that "data." is used to qualify the field

    console.log(template({ name: "John Doe" })); // outputs "<strong>John Doe</strong>"

### touchScroller

Enables kinetic scrolling on touch devices

#### Parameters

##### element `Selector`

The container element to enable scrolling for.
### toString
Formats a `Number` or `Date` using the specified format and the current culture.
#### Returns
`String` the string representation of the formatted value.
#### Formatting numbers and dates
    //format a number using standard number formats and default culture en-US
    kendo.toString(10.12, "n"); //10.12
    kendo.toString(10.12, "n0"); //10
    kendo.toString(10.12, "n5"); //10.12000
    kendo.toString(10.12, "c"); //$10.12
    kendo.toString(0.12, "p"); //12.00 %
    //format a number using custom number formats
    kendo.toString(19.12, "00##"); //0019
    //format a date
    kendo.toString(new Date(2010, 9, 5), "yyyy/MM/dd" ); // "2010/10/05"
    kendo.toString(new Date(2010, 9, 5), "dddd MMMM d, yyyy" ); // "Tuesday October 5, 2010"
    kendo.toString(new Date(2010, 10, 10, 22, 12), "hh:mm tt" ); // "10:12 PM"
#### Parameters

##### value `Date|Number`
The `Date` or `Number` which should be formatted.

##### format `String`
The format string which should be used to format the value.

#### Standard number formats

##### *n* - number
    kendo.culture("en-US");
    kendo.toString(1234.567, "n"); //1,234.57

    kendo.culture("de-DE");
    kendo.toString(1234.567, "n3"); //1.234,567

##### *c* - currency
    kendo.culture("en-US");
    kendo.toString(1234.567, "c"); //$1,234.57

    kendo.culture("de-DE");
    kendo.toString(1234.567, "c3"); //1.234,567 €

##### *p* - percentage (the value is multiplied by 100)
    kendo.culture("en-US");
    kendo.toString(0.222, "p"); //22.20 %

    kendo.culture("de-DE");
    kendo.toString(0.22, "p3"); //22.000 %

##### *e* - exponential
    kendo.toString(0.122, "e"); //1.22e-1
    kendo.toString(0.122, "e4"); //1.2200e-1
#### Custom number formats

Custom number formats can be created by using one or more custom numeric specifiers.

##### *0* - zero placeholder

Replaces the zero with the corresponding digit if one is present; otherwise, zero appears in the result string.
    kendo.toString(1234.5678, "00000"); // 01235

##### *#* - digit placeholder

Replaces the pound sign with the corresponding digit if one is present; otherwise, no digit appears in the result string.
    kendo.toString(1234.5678, "#####"); // 1235

##### *.* - decimal placeholder

Determines the location of the decimal separator in the result string.
    kendo.tostring(0.45678, "0.00"); // 0.46

##### *,* - group separator placeholder
Inserts a group separator between each group of digits.
    kendo.tostring(12345678, "##,#"); // 12,345,678

##### *%* - percentage placeholder
Multiplies a number by 100 and inserts a the percentage symbol (according to the current culture) in the result string.

##### *e* - exponential notation
    kendo.toString(0.45678, "e0"); // 5e-1

##### *;* - section separator

Defines sections of separate format strings for positive, negative, and zero numbers.

##### *"string"|'string'* - literal string
Indicates literal strings which should be included in the result verbatim.

#### Standard date formats
##### *d* - short date pattern
    kendo.toString(new Date(2000, 10, 6), "d"); // 11/6/2000

##### *D* - long date pattern
    kendo.toString(new Date(2000, 10, 6), "D"); // Monday, November 06, 2000

##### *F* - full date/time pattern
    kendo.toString(new Date(2000, 10, 6), "F"); // Monday, November 06, 2000 12:00:00 AM

##### *g* - general date/time pattern (short time)
    kendo.toString(new Date(2000, 10, 6), "g"); // 11/6/2000 12:00 AM

##### *G* - general date/time pattern (long time)
    kendo.toString(new Date(2000, 10, 6), "G"); // 11/6/2000 12:00:00 AM

##### *m|M* - month/day pattern
    kendo.toString(new Date(2000, 10, 6), "m"); // November 06

##### *u* - universal sortable date/time pattern
    kendo.toString(new Date(2000, 10, 6), "u"); // 2000-11-06 00:00:00Z

##### *y|Y* - month/year pattern
    kendo.toString(new Date(2000, 10, 6), "y"); // November, 2000

#### Custom date formats
Custom date formats can be created by using one or more custom date specifiers.

##### *d* - the day of the month, from 1 to 31

##### *dd* - the zero-padded day of the month - from 01 to 31

##### *ddd* - the abbreviated name of the day of the week

##### *dddd* - the full name of the day of the week

##### *f* - the tenths of a second

##### *ff* - the hundreds of a second

##### *fff* - the milliseconds

##### *M* - the month, from 1 to 12

##### *MM* - the zero-padded month, from 01 to 12

##### *MMM* - the abbreviated name of the month

##### *MMMM* - the full name of the month

##### *h* - the hour, using 12-hour clock - from 1 to 12

##### *hh* - the zero-padded hour, using 12-hour clock - from 01 to 12

##### *H* - the hour, using 24-hour clock - from 0 to 23

##### *HH* - the zero-padded hour, using 24-hour clock - from 00 to 23

##### *m* - the minute, from 0 to 59

##### *mm* - the zero-padded minute, from 00 to 59

##### *s* - the second, from 00 to 59

##### *ss* - the zero-padded second, from 00 to 59

##### *tt* - the AM/PM designator

### unbind

Unbinds a tree of HTML elements from a View-Model.
#### Example
    kendo.unbind($("body"));
#### Parameters
##### element `String|jQuery|Node`

The root element(s) from which the unbinding starts. Can be a valid jQuery string selector, a DOM element or a jQuery object.
All child elements are traversed.
