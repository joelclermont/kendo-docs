---
title: Overview
publish: true
---

# TimePicker

The TimePicker HtmlHelper extension is a server-side wrapper for the [Kendo UI TimePicker](http://www.kendoui.com/documentation/ui-widgets/timepicker/overview.aspx) widget.

## Getting Started

Here is how to configure a simple Kendo TimePicker:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

        public ActionResult Index()
        {
            return View();
        }
3.  Add a timepicker:
    - WebForms

            <%: Html.Kendo().TimePicker()
                    .Name("timepicker") //The name of the timepicker is mandatory. It specifies the "id" attribute of the widget.
                    .Min(new DateTime(2010, 1, 1, 10, 0, 0)) //Set min time of the timepicker
                    .Max(new DateTime(2010, 1, 1, 20, 0, 0)) //Set min date of the timepicker
                    .Value(DateTime.Now) //Set the value of the timepicker
            %>
    - Razor

            @(Html.Kendo().TimePicker()
                  .Name("timepicker") //The name of the timepicker is mandatory. It specifies the "id" attribute of the widget.
                  .Min(new DateTime(2010, 1, 1, 10, 0, 0)) //Set min time of the timepicker
                  .Max(new DateTime(2010, 1, 1, 20, 0, 0)) //Set min date of the timepicker
                  .Value(DateTime.Now) //Set the value of the timepicker
            )

## Accessing an Existing TimePicker

You can reference an existing TimePicker instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/timepicker/methods.aspx) to control its behavior.

### Accessing an existing TimePicker instance

    //Put this after your Kendo TimePicker for ASP.NET MVC declaration
    <script>
    $(function() {
        // Notice that the Name() of the timepicker is used to get its client-side instance
        var timepicker = $("#timepicker").data("kendoTimePicker");
    });
    </script>

## Handling Kendo UI TimePicker events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/timepicker/events.aspx) exposed by Kendo UI TimePicker:

### WebForms - subscribe by handler name

    <%: Html.Kendo().TimePicker()
            .Name("timepicker")
            .Events(e => e
                .Open("timepicker_open")
                .Close("timepicker_close")
                .Change("timepicker_change")
            )
    %>
    <script>
    function timepicker_open() {
        //Handle the open event
    }

    function timepicker_close() {
        //Handle the close event
    }

    function timepicker_change() {
        //Handle the change event
    }
    </script>


### Razor - subscribe by handler name

    @(Html.Kendo().TimePicker()
          .Name("timepicker")
          .Events(e => e
                .Open("timepicker_open")
                .Close("timepicker_close")
                .Change("timepicker_change")
          )
    )
    <script>
    function timepicker_open() {
        //Handle the open event
    }

    function timepicker_close() {
        //Handle the close event
    }

    function timepicker_change() {
        //Handle the change event
    }
    </script>

### Razor - subscribe by template delegate

    @(Html.Kendo().TimePicker()
          .Name("timepicker")
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

