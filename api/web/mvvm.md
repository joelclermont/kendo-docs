---
title: kendo.ui.MVVM
tags: api,web
publish: true
---

# kendo.ui.MVVM

## Description



      Model View ViewModel ([MVVM](http://en.wikipedia.org/wiki/Model_View_ViewModel)) is a design pattern which helps developers separate the Model from the View. The View-Model part of MVVM is responsible for
      exposing the data objects from the Model in such a way that those objects are easily consumed in the View.
 


      Kendo MVVM is an implementation of the MVVM pattern which is seamlessly integrated with the rest of the Kendo framework (widgets and DataSource).
 

### Getting Started

#### Binding HTML View to a View-Model

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
       var viewModel = {
          firstName: "John",
          lastName: "Doe",
          displayGreeting: function() {
              // Get the current values of "firstName" and "lastName"
              var firstName = this.get("firstName");
              var lastName = this.get("lastName");
    
              alert("Hello, " + firstName + " " + lastName + "!!!");
          }
       };
       // Bind the View to the View-Model
       kendo.bind($("#view"), viewModel);
     </script>

## Configuration

## Methods

### bind

Binds a tree of HTML elements to a View-Model

#### Binding all children of the BODY to a View-Model

    var viewModel = {
         firstName: "John",
         lastName: "Bar"
    };
    
    kendo.bind($("body"), viewModel);

#### Parameters

##### element `String|Selector|Node`

The root element(s) from which the binding starts. Can be a valid jQuery string selector, a DOM element or a jQuery object.
All child elements are traversed.

##### viewModel `Object`

The View-Model which the elements are bound to.

##### namespace `Object`

Optional namespace too look in when instantiating Kendo widgets. The possible values are kendo.ui and kendo.mobile.ui. The default value is kendo.ui

### unbind

Unbinds a tree of HTML elements from a View-Model.

#### Unbinding all children of the BODY to a View-Model

    kendo.unbind($("body"));

#### Parameters

##### element `String|Selector|Node`

The root element(s) from which the unbinding starts. Can be a valid jQuery string selector, a DOM element or a jQuery object.
All child elements are traversed.

## Events