---
title: Using Kendo UI Declarative Initialization
slug: tutorial-declarative-initialization
tags: Tutorial
publish: true
---

Since the introduction of [Custom Data Attributes][http://dev.w3.org/html5/spec/#custom] in the HTML5 spec,
developers have discovered a whole new world of possibilities.  When you
combine the ability to store arbitrary information in an HTML element with the
power of JavaScript, you get some very interesting alternative development
experiences.

One of the places where it has become very popular in the JavaScript community
at large, is providing information to the underlying JavaScript framework
(such as MVVM) which allows the executing code to mutate the HTML element;
thusly doing things such as binding it to data, transforming it into a custom
UI control or getting configuration values off of it that can’t be stored in
the standard provided HTML attributes.

Kendo UI uses this syntax heavily.  In order to be able to use the full power
of Kendo UI, you really need to know what you can bind with data attributes,
when to use it so it benefits you most and how to use it in concert with Kendo
UI as a whole.  In order to provide some clarity around this, it really needs
to be discussed in two separate contexts.

[### 1. Using the data-bind syntax with MVVM](#using-data-bind-syntax-with-mvvm)

[### 2. Using data- syntax with declarative widget initialization/configuration](#declarative-initialization)


## Using data-bind syntax with MVVM

Lets look at the **data-bind **specific syntax first as it is essential to the
Kendo UI MVVM implementation as well as Knockout. MVVM will not be covered conceptually in this tutorial, but you can go through this article here to get a full explanation on what it is and how to use it.

Assume that we have a simple select list and we want to bind it to the view
model.  We declare the HTML and the view model.

This is very basic, but we are using the **data-bind **to bind the source of
the select to the view model **things** array.  Also note that you can bind to
a function as well as I’m doing with **data-bind=”text: thingSelection” **on
the **h2**.

But the question now becomes, what else can I bind and how do I do it?

This is well documented in our [Getting Started][http://docs.kendoui.com/getting-started/framework/mvvm/overview] section of the documentation.
On the *mvvm* section, you will find a high level explanation of how to
bind with the Kendo UI MVVM framework.  Under the [Bindings][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/attr] sub-topic, you
will find a complete list of what you can bind to.  For reference, I have
included that list here as well.

  * [Attr][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/attr]

  * [Checked][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/checked]
  
  * [Click][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/click] 

  * [Disabled][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/disabled]

  * [Enabled][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/enabled]

  * [Event][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/event]

  * [Html][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/html]

  * [Source][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/source]

  * [Style][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/style]

  * [Text][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/text]

  * [Value][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/value]

We have provided samples with each of these binding declarations to help you
understand how and when you can use them.

For instance, lets look at styling the drop down a bit using the data-bind
syntax with style.  I can set the drop down width as well as setting its
margins by using data-bind and the above referenced style.


    data-bind="style: { width: thingsWidth, fontSize: thingsFontSize}"


The width and font-size are now bound to view model properties and the select
element will be styled appropriately based on the values in the view model.
The **h2 **also has its color bound to the view model.  When those properties
change, so will the style on the select element.  Feel free to try it for
yourself in the above fiddle.

Whenever you are referencing a css property that has a dash, you eliminate the
dash and use lower camel case notation (i.e. fontSize instead of font-size) as
is documented [here][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/style#using-style-attributes-which-contain-a-dash].

## Declarative Initialization

The other way of using **data** attributes with Kendo UI is something that we
call Declarative Initialization.  This is the concept of initializing widgets
and configuring those widgets with data attributes instead of having to select
each element that we want to turn into a widget and configure it with
JavaScript.

Let’s take a look at the above example using Declarative Initialization to
turn the select into a Kendo UI DropDown List.  We do this by setting the
**data-role** attribute to **dropdownlist.**  Normally this would be done by
calling **kendoDropDownList **on the element.  Thanks to declarative binding,
we don’t have to do that anymore.

Notice that we lost our previous styling.  This is because the ordinary select
is now a Kendo UI DropDown which has it’s own styling.  Everything else keeps
right on working exactly they way you would expect.

Now we could have several drop downs on a page and we only need to configure
them with declarative data attributes instead of having to select each and
every one with jQuery and call the **kendoDropDownList **method on them.

>It has always been our goal to not force things on you.  Declarative
Bindings are powerful, but you don’t need to buy into the MVVM pattern to use
them.

Let’s rework the above example and get rid of the view model, but this time
we’ll bind it to a DataSource and let declarative initialization do all the
work for us.

The **kendo.init **call will initialize whatever piece of the UI is passed in
as a reference. Notice that I am only calling **init** on the **main **div.
For maximum performance, specify the container for Kendo UI to initialize so
it doesn’t have to walk the entire document to find the relevant widgets.

You can see that I have supplied configuration attributes for the drop down
list such as **data-source **which binds the drop down to the Kendo UI
DataSource.  Also, I have specified configuration attributes like **data-text-
field** and **data-value-field**.  You can specify any configuration value
with declarative initialization, and it will work.  Attributes like
**dataTextField** become **data-text-field**.  Bindings are specified as lower
case separated by dashes.

Events can be bound as well. Above, I bind to the **change** event.  When the
event is called, **this **will be the object that fired the event.  In this
case, that’s our drop down list.  I can then get its **text** value and update
the **h2** tag.

## IMPORTANT THINGS TO KNOW

1. Bindings are not JavaScript.  Do not try and do this…


    data-bind="value: if ($(“#div”).html() === “somevalue”)…

That won’t work.  You should be doing that in your view model.  If you aren’t
using a view model and you have a good use case for sticking JavaScript into
your markup, consider using a [Kendo UI Template][http://demos.kendoui.com/web/templates/index.html] instead.

2. Kendo UI is not the only framework that uses data attributes for binding.
In fact, its pretty common.  If you find yourself in a situation where you
need to mitigate collisions with Kendo UI and some other JS library, you can
provide a namespace for Kendo UI and then reference that namespace instead.


    kendo.ns="kendo";

    // then
    data-bind="value: someValue" 

	// becomes
    data-kendo-bind="value: someValue"


## Don’t Do Guesswork!

It’s easy when you start using these bindings to try and guess what you can
and can’t do.  Instead, refer to the docs for the MVVM framework bindings
[here][http://docs.kendoui.com/getting-started/framework/mvvm/overview], and the standard widget declarative bindings [here][http://docs.kendoui.com/getting-started/framework/mvvm/bindings/attr].  When
doing initialization of widgets using configuration attributes in the
declarative bindings, simply look up the configuration values so you know what
you can and can’t use to configure the widget.