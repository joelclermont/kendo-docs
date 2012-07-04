---
title: Attr
slug: mvvm-attribute-binding
publish: true
---

### Attr binding

The `attr` binding populates DOM element attributes from View-Model fields or methods. This is useful in many cases - setting the `href` and `title` of a hyperlink, setting the `src` attribute of an image etc. If the View-Model field(s) change the attributes would be updated. The `attr` binding is set like this: `attr: { attribute1: field1, attribute2: field2 }` where `attribute1` and `attribute2` are the names of the attributes that would be set and `field1` and `field2` are the names of the View-Model fields to which those attributes would be bound.&nbsp;
  

#### Example of the `attr` binding
 
    <img id="logo" data-bind="attr: { src: imageSource, alt: imageAlt }" />
    <script>
    var viewModel = kendo.observable({
        imageSource: "http://www.kendoui.com/image/kendo-logo.png",
        imageAlt: "Kendo Logo"
    });
    
    kendo.bind($("#logo"), viewModel);
    </script>
       

In this example the `src` and `alt` attributes of the image are bound to the View-Model. After calling `kendo.bind` the image would look like this (`data-bind` attribute is removed for clarity):

 
    <img id="logo" src="http://www.kendoui.com/image/kendo-logo.png" alt="Kendo Logo"" />
     

Changing the `imageSource` or `imageSource` fields would update the `src` and `alt` attributes respectively.

### Important: value and checked attribute binding

If you want to set the `value` or `checked` attributes use the [value](http://www.kendoui.com/documentation/framework/mvvm/bindings/Value.aspx) and [checked](http://www.kendoui.com/documentation/framework/mvvm/bindings/Checked.aspx) bindings instead.

### Note: data attributes

You can also set HTML5 data attributes via the `attr` binding:

  

#### Setting data attributes via the `attr` binding
 
    <div data-bind="attr: { data-foo: fooValue, data-bar: barValue }">
    <script>
    var viewModel = kendo.observable({
        fooValue: "foo",
        barValue: "bar"
    });
    
    kendo.bind($("div"), viewModel);
    </script>
      </div> 

### Widget support

The `attr` binding is **not** support by Kendo Widgets.