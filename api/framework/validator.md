---
title: kendo.ui.Validator
tags: api,web
publish: true
---

# kendo.ui.Validator

Validator offers an easy way to do client-side form validation.
Built around the HTML5 form validation attributes it supports variety of built-in validation rules, but also provides a convenient way for setting custom rules handling.

#### **Validator** initialization to validate input elements inside a container

     <div id="myform">
      <input type="text" name="firstName" required />
      <input type="text" name="lastName" required />
      <button id="save" type="button">Save</button>
     </div>

     <script>
      $(document).ready(function(){
          var validatable = $("#myform").kendoValidator().data("kendoValidator");
          $("#save").click(function() {
             if (validatable.validate()) {
                 save();
             }
          });
      });
      </script>

#### Validation Rules

#### **required**- element should have a value

     <input type="text" name="firstName" required />

#### **pattern**- constrains the value to match a specific regular expression

     <input type="text" name="twitter" pattern="https?://(?:www\.)?twitter\.com/.+i" />

#### **max/min**- constrain the minimum and/or maximum numeric values that can be entered

     <input type="number" name="age" min="1" max="42" />

#### **step**- when used in combination with the min and max attributes, constrains the granularity of values that can be entered

     <input type="number" name="age" min="1" max="100" step="2" />

#### **url**- constrain the value to being a valid URL

     <input type="url" name="url" />

#### **email**- constrain the value to being a valid email

     <input type="email" name="email" />

Beside the built-in validation rules, KendoUI Validator also provides a convenient way for setting custom rules through its rules configuration option.

####
     $("#myform").kendoValidator({
         rules: {
           custom: function(input) {
             // Only Tom will be a valid value for FirstName input
             return input.is("[name=firstname]") && input.val() === "Tom";
           }
         }
    });

#### Validation Messages

There are several ways to control the messages which appears if validation fails:

#### Set the validation messages for all input elements, through configuration options

      $("#myform").kendoValidator({
         rules: {
             custom: function(input) {
                     //...
             }
         },
         messages: {
           // defines message for the 'custom' validation rule
           custom: "Please enter valid value for my custom rule",
           // overrides the built-in message for required rule
           required: "My custom required message",
           // overrides the built-in email rule message with a custom function which return the actual message
           email: function(input) {
             return getMessage(input);
           }
        }
     });

#### Use the title and validationMessage attributes to set per input element messages

        <input type="tel" pattern="\d{10}" validationMessage="Plase enter a ten digit phone number" />

#### Triggering validation

In order to trigger the element(s) validation, **validate** method should be used. It will return either _true_ if validation succeeded or _false_ in case of a failure.


 Note that if a HTML form element is set as validation container, the form submits will be automatically prevented if validation fails.


#### Initialize Kendo Validator with specific tooltip position


     Ideally Kendo Validator places its tooltips besides the validated input. However, if the input is later enhanced to a ComboBox, AutoComplete or other Kendo Widget, placing the
     tooltip beside the input may cover important information or break the widget rendering. In this case, you can specify where exactly do you want the tooltip to be placed by
     adding a span with data-for attribute set to the validated input name and a class .k-invalid-msg. Check the example below:


#### **Validator** initialization with specific tooltip placement (the tooltip will remain outside of the AutoComplete widget after enhancement)

     <div id="myform">
         <input type="text" id="name" name="name" required />
         <span class="k-invalid-msg" data-for="name"></span>
     </div>

     <script>
         $("#name").kendoAutoComplete({
                        dataSource: data,
                        separator: ", "
                    });

         $("#myform").kendoValidator();
     </script>

## Configuration

### messages `Object`

Set of messages (either strings or functions) which will be shown when given validation rule fails.
 By setting already existing key the appropriate built-in message will be overridden.

#### Example

    $("#myform").kendoValidator({
         rules: {
             custom: function(input) {
                //...
             }
         },
         messages: {
             custom: "Please enter valid value for my custom rule",// defines message for the 'custom' validation rule
             required: "My custom required message", // overrides the built-in message for required rule
             email: function(input) { // overrides the built-in email rule message with a custom function which return the actual message
                 return getMessage(input);
             }
         }
    });

### rules `Object`

Set of validation rules. Those rules will extend the built-in ones.

#### Example

    $("#myform").kendoValidator({
         rules: {
             custom: function(input) {
                 return input.is("[name=firstname]") && input.val() === "Tom"; // Only Tom will be a valid value for FirstName input
             }
         }
    });

### validateOnBlur `Boolean`

Determines if validation will be triggered when element loses focus. Default value is true.

## Methods

### errors

Get the error messages if any.

#### Example

    // get a reference to the validatable form
    var validatable = $("#myform").kendoValidator().data("kendoValidator");
    $("#save").click(function() {
        if (validatable.validate() === false) {
            // get the errors and write them out to the "errors" html container
            var errors = validatable.errors();
            $(errors).each(function() {
                $("#errors").html(this);
            });
        }
    });

#### Returns

`Array` Messages for the failed validation rules.

### validate

Validates the input element(s) against the declared validation rules.

#### Example

    // get a reference to the validatable form
    var validatable = $("#myform").kendoValidator().data("kendoValidator");
    // check validation on save button click
    $("#save").click(function() {
        if (validatable.validate()) {
            save();
        }
    });

#### Returns

`Boolean` If all rules are passed successfully.

### validateInput

Validates the input element against the declared validation rules.

#### Parameters

##### input `Element`

Input element to be validated.

#### Returns

`Boolean` If all rules are passed successfully.
