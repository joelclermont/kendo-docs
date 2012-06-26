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
### unbind

Unbinds a tree of HTML elements from a View-Model.
#### Example
    kendo.unbind($("body"));
#### Parameters
##### element `String|jQuery|Node`

The root element(s) from which the unbinding starts. Can be a valid jQuery string selector, a DOM element or a jQuery object.
All child elements are traversed.
