# kendo.Template

## Description



 Templates offer way of creating HTML chunks. Options such as HTML encoding and compilation for optimal
 performance are available.

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

#### Use javascript in templates

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

## Configuration

## Methods

## Events