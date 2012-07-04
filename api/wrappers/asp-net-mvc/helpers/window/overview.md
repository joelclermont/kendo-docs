---
title: Overview
slug: mvc-window-overview
publish: true
---

# Window

The Window HtmlHelper extension is a server-side wrapper for the [Kendo UI Window](http://www.kendoui.com/documentation/ui-widgets/window/overview.aspx) widget.

## Getting Started

There are two ways to populate the content of the Kendo Window for ASP.NET MVC

*   server - define content of the window on server.
*   ajax - window will get the content with ajax request

### Configure the Kendo Window with a content defined on the server

Here is how to configure the Kendo Window:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

        public ActionResult Index()
        {
            return View();
        }
3.  Add a window:
    - WebForms

            <% Html.Kendo().Window()
                   .Name("window") //The name of the window is mandatory. It specifies the "id" attribute of the widget.
                   .Title("About Alvar Aalto") //set the title of the window
                   .Content(() => //define the content of the window
                   {
                       %>
                           Static content of the Window
                       <%
                   })
                   .Draggable() //Enable dragging of the window
                   .Resizable() //Enable resizing of the window
                   .Width(600)  //Set width of the window
                   .Render(); //render the window
            %>
    - Razor

            @(Html.Kendo().Window()
                  .Name("window") //The name of the window is mandatory. It specifies the "id" attribute of the widget.
                  .Title("About Alvar Aalto") //set the title of the window
                  .Content(@<text> //define the content of the window
                          Static content of the Window
                  </text>)
                  .Draggable() //Enable dragging of the window
                  .Resizable() //Enable resizing of the window
                  .Width(600)  //Set width of the window
            )

### Configure the Kendo Window with a load-on-demand content

Here is how to configure the Kendo Window:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

        public ActionResult Index()
        {
            return View();
        }
3.  Create an action method which renders the content:

        public ActionResult AjaxContent()
        {
            return View();
        }
4.  Add a window:
    - WebForms

            <% Html.Kendo().Window()
                   .Name("window") //The name of the window is mandatory. It specifies the "id" attribute of the widget.
                   .Title("About Alvar Aalto") //set the title of the window
                   .LoadContentFrom("AjaxContent", "Window") //define the Action and Controller name
            %>
    - Razor

            @(Html.Kendo().Window()
                  .Name("window") //The name of the window is mandatory. It specifies the "id" attribute of the widget.
                  .Title("About Alvar Aalto") //set the title of the window
                  .LoadContentFrom("AjaxContent", "Window") //define the Action and Controller name
            )

## Accessing an Existing Window

You can reference an existing Window instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/window/methods.aspx) to control its behavior.

### Accessing an existing Window instance

    //Put this after your Kendo Window for ASP.NET MVC declaration
    <script>
    $(function() {
        // Notice that the Name() of the window is used to get its client-side instance
        var window = $("#window").data("kendoWindow");
    });
    </script>


## Handling Kendo UI Window events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/window/events.aspx) exposed by Kendo UI Window:

### WebForms - subscribe by handler name

    <%: Html.Kendo().Window()
            .Name("window")
            .Events(e => e
                .Open("window_open")
            .Close("window_close")
        )
    %>
    <script>
    function window_open() {
        //Handle the open event
    }

    function window_close() {
        //Handle the close event
    }
    </script>


### Razor - subscribe by handler name

    @(Html.Kendo().Window()
          .Name("window")
          .Events(e => e
                .Open("window_open")
                .Close("window_close")
          )
    )
    <script>
    function window_open() {
        //Handle the open event
    }

    function window_close() {
        //Handle the close event
    }
    </script>


### Razor - subscribe by template delegate

    @(Html.Kendo().Window()
          .Name("window")
          .Events(e => e
              .Open(@<text>
                function() {
                    //Handle the open event inline
                }
              </text>)
              .Close(@<text>
                function() {
                    //Handle the close event inline
                }
                </text>)
          )
    )

