---
title: MVVM Features in Kendo UI
slug: gs-mvvm-features-in-kendo-ui
tags: tutorial, mvvm
related: mvvm-overview
publish: true
---

# MVVM in Kendo UI Walkthrough

This document provides an in-depth look on creating Kendo UI apps that use framework MVVM features. For those not familiar with the term **MVVM**, we'll start by setting some context.

## A Brief MVVM Primer

### The Problem

We’ve seen an unprecedented increase in the amount of devices and operating systems in the past few years. We have desktops, laptops, tablets, phones, netbooks and even devices that connect right to your TV (read Roku, Apple TV). The only way that you can deliver content on all of these platforms without writing dozens of applications, is to write a web application. These web applications are becoming more and more complex on the client side. AJAX is an important part of modern web applications and there is an increasing need to model data in the client as well as on the server. 

You may be familiar with the phrase “Single Page Application”, or an **SPA. **The best example of an** **SPA is probably [Gmail](http://gmail.google.com). The idea is that when you visit the application and click on actions, instead of the entire page being sent to the server and then a new page being sent back, only the relevant portion of the UI is changed. This is done by making background requests for data to the server and then updating the UI. This can make for very complex scenarios in a UI as you try and keep up with changes that are happening with your data on the server, the data as it’s changed in the UI, and the current overall state of the application.

### The Solution

One of the ways that people are handling this is with different architecture patterns on the front-end like [MVP](http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93presenter), [MVC](http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) or [MVVM](http://en.wikipedia.org/wiki/Model_View_ViewModel). You may be familiar with [BackboneJS](http://documentcloud.github.com/backbone/), [KnckoutJS](http://knockoutjs.com/) or [EmberJS](http://emberjs.com/). These are all implementations of various patterns which attempt to help you organize and manage your UI while alleviating the need for you to manually keep track of all the changes.

MVVM is short for Model View View-Model. Kendo UI has a full MVVM framework baked right into it’s core with this beta release. Lets take a look at how MVVM makes your life more awesome, and how it works seamlessly with Kendo UI.

> If you have been using MVVM and Knockout for some time and have questions about why we decided to make MVVM part of the Kendo UI core, please read [this post](http://www.kendoui.com/blogs/teamblog/posts/12-02-16/kendo_ui_mvvm_and_knockoutjs.aspx).

## MVVM In Kendo UI

Lets look at a simple scenario and how we might typically build this application, then we’ll back up and engineer it with the MVVM pattern. 

### An Example of Developing Without MVVM

Let's take a look at how one might build a simple list application without MVVM (click the JavaScript and HTML tabs of the embedded fiddle to view the code).

<iframe frameborder="0" allowfullscreen="allowfullscreen" src="http://jsfiddle.net/NqSuS/embedded/result,js,html" style="width: 100%; height: 300px;"></iframe>

This is typical. Bind the button to an event handler, select the DOM elements, update the table with a new row and then clear the DOM elements back out. All manually. The only way we could make this easier is by doing some templating instead of creating the row dynamically with HTML in the JavaScript.

### Developing With MMVM

Let's see how the new MVVM pattern in Kendo UI can really make life easier.

The first thing that we need to do is to create a view model. A view model is an observable object. This object has properties and methods. Each property will be bound to something in the HTML. This binding is two way, meaning that if the binding changes on the UI, the model changes and vice versa.

#### The ViewModel

Here is what the **ViewModel** looks like.

	viewModel = kendo.observable({
	    // expenses array will hold the grid values
    	expenses: [],
	    
	    // type array populates the drop down
    	type: [
    		{ name: "Food", value: "food"}, 
    		{ name: "Merchant", value: "merchant"}, 
    		{ name: "Bills", value: "bills" }
    	],
    	
    	// expenseType holds the currently selected value of the dropdown list
     	expenseType: "food", 

     	// the values are bound to the merchant and amount fields
     	merchant: null,
     	amount: null,

     	// event to execute on click of add button
     	create: function(e) {

	        // add the items to the array of expenses 
	        this.get("expenses").push({Type: this.get("expenseType"), 
	                                   Merchant: this.get("merchant"), 
	                                   Amount: this.get("amount")});

	        // reset the form this.set("expenseType", "food");
	        this.set("merchant", "");
	        this.set("amount", "");
    	}
	});

	// apply the bindings
	kendo.bind(document.body.children, viewModel);

You can see from the comments inline that we have moved some things out of the markup and into the view model. Lets break it down…

**expenses**: Instead of using a plain HTML table to display the values from our input form, we are going to use a Kendo UI Grid. It’s a much better user experience. The **expenses **array holds the values that the grid will use as is source.

**type:** Remember the select element? Instead of defining the items inline with options in the HTML, we are going to bind the element to this array. We’ll also apply some Kendo UI magic to this boring dropdown.

**expenseType:** This variable will be bound to whatever value is currently selected in the above mentioned dropdown.

**merchant:** Bound to the value of the **merchant** input box.

**amount:** Bound to the value of **amount **input box.

**create:** This is the event that will be fired by the **Add **button. Inside the event, we are going to do following:

**kendo.bind(document.body.children, viewModel):** The statement that initializes the binding between the view model and the relevant HTML.

#### The View (Markup)

We additionally need to make some changes in our markup. Lets take it element by element and examine the bindings:

	<select data-role="dropdownlist" data-bind="source: type, value: expenseType">
		<span data-text-field="name" data-value-field="value" >
	</select>

The **select** element now has no options. Instead, it has some new **data** attributes.

	<dt>Merchant</dt>
	<dd>
		<input id="merchant" type="text" class='k-textbox' data-bind="value: merchant" />
	</dd>

The **merchant **input has a new binding. The **data-bind=”value: merchant”** says that we want to bind the value of this input to the **merchant** variable in the view model. I aslo added a “**k-textbox**” css class to it to make it pretty.

	<dt>Amount</dt> 
	<dd>
		<input data-role="numerictextbox" data-bind="value: amount" id="amount" type="text" />
	</dd>

The **amount** input has two new bindings:

	<button id="create" data-bind="click: create" class="k-button">Add</button>

The **Add** button has only one new change. It now has a **data-bind=”click: create”**. This binds its click event to the **create** function in the view model. It’s crazy how easy this is.

	<div data-role="grid" data-sortable="true" data-bind="source: expenses"
    	 data-columns='["Type", "Merchant", "Amount"]' ></div>

This last one is the grid. Yes, this one line creates a [Kendo UI Grid](http://demos.kendoui.com/web/grid/index.html).

### The Final Result

Here is the finished product. Kendo UI bindings are keeping the UI and the model in sync as changes are made.

<iframe frameborder="0" allowfullscreen="allowfullscreen" src="http://jsfiddle.net/burkeholland/NqSuS/6/embedded/result,js,html" style="width: 100%; height: 450px;"></iframe>

Not only does MVVM keep you from having to worry about many of the manual details, it also dramatically simplifies your code so that in your JavaScript you are only working with model objects. The DOM simply reflects the changes that you make to the model.
