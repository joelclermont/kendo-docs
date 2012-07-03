---
title: MVVM Text Binding
slug: mvvm-text-binding
publish: true
---

### Text binding

The `text` binding sets the text content of the target DOM element to a View-Model value. Changing the View-Model value via code will
update the text of the DOM element. If the View-Model value is not of primitive type (Text, Number or Date)
the result returned by the `toString` JavaScript method will be used as the value.

To set the value displayed by an `input`, `textarea` or `select`
use the [value](http://www.kendoui.com/documentation/framework/mvvm/bindings/value.aspx) binding instead.

  

#### Use the text binding
 
    <span data-bind="text: name"></span>
    <script>
    var viewModel = kendo.observable({
        name: "John Doe"
    });
    
    kendo.bind($("span"), viewModel);
    </script>
      

The output will be (the data-bind attribute is removed for clarity):
 
    <span>John Doe</span>
     

If the View-Model value contains HTML tags those will be output verbatim. For example this:

 
    <span data-bind="text: name"></span>
    <script>
    var viewModel = kendo.observable({
        name: "<strong>John Doe</strong>"
    });
    
    kendo.bind($("span"), viewModel);
    </script>
     

will output visible HTML tags.