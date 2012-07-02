---
title: Overview
publish: true
---

### NumericTextBox

The NumericTextBox HtmlHelper extension is a server-side wrapper for the [Kendo UI NumericTextBox](http://www.kendoui.com/documentation/ui-widgets/numerictextbox/overview.aspx) widget.

### Getting Started

Here is how to configure a simple Kendo NumericTextBox:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

    public ActionResult Index()
    {
    return View();
    }
        3.  Add a numerictextbox:

#### WebForms
 
    <%: Html.Kendo().NumericTextBox()
        .Name("numerictextbox") //The name of the numerictextbox is mandatory. It specifies the "id" attribute of the widget.
        .Min(-100) //Set min value of the numerictextbox
        .Max(100) //Set min value of the numerictextbox
        .Value(10) //Set the value of the numerictextbox
    %>
              
#### Razor
 
    <pre class="prettyprint">@(Html.Kendo().NumericTextBox()
        .Name("numerictextbox") //The name of the numerictextbox is mandatory. It specifies the "id" attribute of the widget.
        .Min(-100) //Set min value of the numerictextbox
        .Max(100) //Set min value of the numerictextbox
        .Value(10) //Set the value of the numerictextbox
    ) </pre>  

### Accessing an Existing NumericTextBox

You can reference an existing NumericTextBox instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/numerictextbox/methods.aspx) to control its behavior.

  

#### Accessing an existing NumericTextBox instance
 
    //Put this after your Kendo NumericTextBox for ASP.NET MVC declaration
    <script>
    $(function() { 
    // Notice that the Name() of the numerictextbox is used to get its client-side instance
    var grid = $("#numerictextbox").data("kendoNumericTextBox");
    });
    </script>
      

### Handling Kendo UI NumericTextBox events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/numerictextbox/events.aspx) exposed by Kendo UI NumericTextBox:

  

#### WebForms - subscribe by handler name
 
    <%: Html.Kendo().NumericTextBox()
        .Name("numerictextbox")
        .Events(e => e
            .Change("numerictextbox_change")
            .Spin("numerictextbox_spin")
        )
    %>
    <script>
    function numerictextbox_spin() {
        //Handle the spin event
    }
    
    function numerictextbox_change() {
        //Handle the change event
    }
    </script>
       

#### Razor - subscribe by handler name
 
    @(Html.Kendo().NumericTextBox()
      .Name("numerictextbox")
      .Events(e => e
            .Change("numerictextbox_change")
            .Spin("numerictextbox_spin")
      )
    )
    <script>
    function numerictextbox_spin() {
        //Handle the spin event
    }
    
    function numerictextbox_change() {
        //Handle the change event
    }
    </script>
       

#### Razor - subscribe by template delegate
 
    @(Html.Kendo().NumericTextBox()
      .Name("numerictextbox")
      .Events(e => e
          .Change(@<text>
            function() {
                //Handle the change event inline
            }
          </text>)
          .Spin(@<text>
            function() {
                //Handle the spin event inline
            }
            </text>)
      )
    )
     