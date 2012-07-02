---
title: Overview
publish: true
---

### DateTimePicker

The DateTimePicker HtmlHelper extension is a server-side wrapper for the Kendo UI DateTimePicker widget.

### Getting Started

Here is how to configure a simple Kendo DateTimePicker:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

    public ActionResult Index()
    {
    return View();
    }
        3.  Add a datetimepicker:

#### WebForms
 
    <%: Html.Kendo().DateTimePicker()
        .Name("datetimepicker") //The name of the datetimepicker is mandatory. It specifies the "id" attribute of the widget.
        .Min(new DateTime(2010, 1, 1, 10, 0, 0)) //Set min time of the datetimepicker
        .Max(new DateTime(2010, 1, 1, 20, 0, 0)) //Set min date of the datetimepicker
        .Value(DateTime.Now) //Set the value of the datetimepicker
    %>
              
#### Razor
 
    <pre class="prettyprint">@(Html.Kendo().DateTimePicker()
        .Name("datetimepicker") //The name of the datetimepicker is mandatory. It specifies the "id" attribute of the widget.
        .Min(new DateTime(2010, 1, 1, 10, 0, 0)) //Set min time of the datetimepicker
        .Max(new DateTime(2010, 1, 1, 20, 0, 0)) //Set min date of the datetimepicker
        .Value(DateTime.Now) //Set the value of the datetimepicker
    
    ) </pre>  

### Accessing an Existing DateTimePicker

You can reference an existing DateTimePicker instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the API to control its behavior.

  

#### Accessing an existing DateTimePicker instance
 
    //Put this after your Kendo DateTimePicker for ASP.NET MVC declaration
    <script>
    $(function() { 
    // Notice that the Name() of the datetimepicker is used to get its client-side instance
    var grid = $("#datetimepicker").data("kendoDateTimePicker");
    });
    </script>
      

### Handling Kendo UI DateTimePicker events

You can subscribe to all events exposed by Kendo UI DateTimePicker:

  

#### WebForms - subscribe by handler name
 
    <%: Html.Kendo().DateTimePicker()
        .Name("datetimepicker")
        .Events(e => e
            .Open("datetimepicker_open")
            .Close("datetimepicker_close")
            .Change("datetimepicker_change")
        )
    %>
    <script>
    function datetimepicker_open() {
        //Handle the open event
    }
    
    function datetimepicker_close() {
        //Handle the close event
    }
    
    function datetimepicker_change() {
        //Handle the change event
    }
    </script>
       

#### Razor - subscribe by handler name
 
    @(Html.Kendo().DateTimePicker()
      .Name("datetimepicker")
      .Events(e => e
            .Open("datetimepicker_open")
            .Close("datetimepicker_close")
            .Change("datetimepicker_change")
      )
    )
    <script>
    function datetimepicker_open() {
        //Handle the open event
    }
    
    function datetimepicker_close() {
        //Handle the close event
    }
    
    function datetimepicker_change() {
        //Handle the change event
    }
    </script>
       

#### Razor - subscribe by template delegate
 
    @(Html.Kendo().DateTimePicker()
      .Name("datetimepicker")
      .Events(e => e
          .Open(@<text>
            function() {
                //Handle the open event inline
            }
          </text>)
          .Change(@<text>
            function() {
                //Handle the change event inline
            }
            </text>)
      )
    )
     