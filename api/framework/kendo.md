---
title: kendo
tags: api,framework
publish: true
---

# kendo

## Methods

### htmlEncode

Encodes HTML characters to entities.

#### Example
    var html = kendo.htmlEncode("<span>Hello</span>");
    console.log(html); // outputs "&lt;span&gt;Hello&lt;/span&gt;&quot;"

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
