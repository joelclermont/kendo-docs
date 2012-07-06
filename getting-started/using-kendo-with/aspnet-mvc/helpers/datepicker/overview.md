---
title: Overview
slug: mvc-datepicker-overview
publish: true
---

# DatePicker

The DatePicker HtmlHelper extension is a server-side wrapper for the [Kendo UI DatePicker](http://www.kendoui.com/documentation/ui-widgets/datepicker/overview.aspx) widget.

## Getting Started

Here is how to configure a simple Kendo DatePicker:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

        public ActionResult Index()
        {
            return View();
        }
3.  Add a datepicker:
    - WebForms

            <%: Html.Kendo().DatePicker()
                .Name("datepicker") //The name of the datepicker is mandatory. It specifies the "id" attribute of the widget.
                .Min(new DateTime(1900, 1, 1)) //Set min date of the datepicker
                .Max(new DateTime(2099, 12, 31)) //Set min date of the datepicker
                .Value(DateTime.Today) //Set the value of the datepicker
            %>
    - Razor

            @(Html.Kendo().DatePicker()
                .Name("datepicker") //The name of the datepicker is mandatory. It specifies the "id" attribute of the widget.
                .Min(new DateTime(1900, 1, 1)) //Set min date of the datepicker
                .Max(new DateTime(2099, 12, 31)) //Set min date of the datepicker
                .Value(DateTime.Today) //Set the value of the datepicker
            )

## Accessing an Existing DatePicker

You can reference an existing DatePicker instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/datepicker/methods.aspx) to control its behavior.


### Accessing an existing DatePicker instance

    //Put this after your Kendo DatePicker for ASP.NET MVC declaration
    <script>
    $(function() {
    // Notice that the Name() of the datepicker is used to get its client-side instance
    var datepicker = $("#datepicker").data("kendoDatePicker");
    });
    </script>


### Handling Kendo UI DatePicker events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/datepicker/events.aspx) exposed by Kendo UI DatePicker:



### WebForms - subscribe by handler name

    <%: Html.Kendo().DatePicker()
        .Name("datepicker")
        .Events(e => e
            .Open("datepicker_open")
            .Close("datepicker_close")
            .Change("datepicker_change")
        )
    %>
    <script>
    function datepicker_open() {
        //Handle the open event
    }

    function datepicker_close() {
        //Handle the close event
    }

    function datepicker_change() {
        //Handle the change event
    }
    </script>


### Razor - subscribe by handler name

    @(Html.Kendo().DatePicker()
      .Name("datepicker")
      .Events(e => e
            .Open("datepicker_open")
            .Close("datepicker_close")
            .Change("datepicker_change")
      )
    )
    <script>
    function datepicker_open() {
        //Handle the open event
    }

    function datepicker_close() {
        //Handle the close event
    }

    function datepicker_change() {
        //Handle the change event
    }
    </script>


### Razor - subscribe by template delegate

    @(Html.Kendo().DatePicker()
      .Name("datepicker")
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

