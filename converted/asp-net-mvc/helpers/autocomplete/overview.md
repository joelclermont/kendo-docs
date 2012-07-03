---
title: Overview
publish: true
---

# AutoComplete

The AutoComplete HtmlHelper extension is a server-side wrapper for the [Kendo UI AutoComplete](http://www.kendoui.com/documentation/ui-widgets/autocomplete/overview.aspx) widget.

## Getting Started

There are two ways to bind a Kendo AutoComplete for ASP.NET MVC:

*   **server** - the data will be serialized to the client. No Ajax requests will be made.
*   **ajax** - the autocomplete will make ajax requests to get the data.

### Configure the Kendo AutoComplete for server binding

Here is how to configure the Kendo AutoComplete for server binding to the Northwind Products table using Linq to SQL:

 1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.
 2.  Create a new action method and pass the Products table as the model:

        public ActionResult Index()
        {
            NorthwindDataContext northwind = new NorthwindDataContext();

            return View(northwind.Products);
        }
 3.  Make your view strongly typed:
     - WebForms

        <%@ Page Language="C#" MasterPageFile="~/Views/Shared/Site.Master"
        Inherits="System.Web.Mvc.ViewPage<IEnumerable<MvcApplication1.Models.Product>>" %>
     - Razor

             @model IEnumerable<MvcApplication1.Models.Product>
 4.  Add a server bound autocomplete:
     - WebForms

             <%: Html.Kendo().AutoComplete()
                 .Name("productAutoComplete") //The name of the autocomplete is mandatory. It specifies the "id" attribute of the widget.
                 .DataTextField("ProductName") //Specifies which property of the Product to be used by the autocomplete.
                 .BindTo(Model)   //Pass the list of Products to the autocomplete.
                 .Filter("contains") //Define the type of the filter, which autocomplete will use.
             %>
     - Razor

             @(Html.Kendo().AutoComplete()
               .Name("productAutoComplete") //The name of the autocomplete is mandatory. It specifies the "id" attribute of the widget.
               .DataTextField("ProductName") //Specifies which property of the Product to be used by the autocomplete.
               .BindTo(Model)   //Pass the list of Products to the autocomplete.
               .Filter("contains") //Define the type of the filter, which autocomplete will use.
             )

### Configure the Kendo AutoComplete for ajax binding

Here is how to configure the Kendo AutoComplete for ajax binding to the Northwind Products table using Linq to SQL:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.
2.  Create an action method which renders the view:
    public ActionResult Index()
    {
        return View();
    }
3.  Create a new action method and pass the Products table as Json result:
    public JsonResult GetProducts()
    {
        NorthwindDataContext northwind = new NorthwindDataContext();

        return Json(northwind.Products);
    }
4.  Add a ajax bound autocomplete:
     - WebForms

             <%: Html.Kendo().AutoComplete()
                 .Name("productAutoComplete") //The name of the autocomplete is mandatory. It specifies the "id" attribute of the widget.
                 .DataTextField("ProductName") //Specifies which property of the Product to be used by the autocomplete.
                 .DataSource(source =>
                 {
                         source.Read(read =>
                        {
                                 read.Action("GetProducts", "Home") //Set the Action and Controller name
                                     .ServerFiltering(true); //If true the DataSource will not filter the data on the client.
                        });
                 })
             %>
     - Razor

             @(Html.Kendo().AutoComplete()
               .Name("productAutoComplete") //The name of the autocomplete is mandatory. It specifies the "id" attribute of the widget.
               .DataTextField("ProductName") //Specifies which property of the Product to be used by the autocomplete.
               .DataSource(source =>
                 {
                         source.Read(read =>
                        {
                                 read.Action("GetProducts", "Home") //Set the Action and Controller name
                                     .ServerFiltering(true); //If true the DataSource will not filter the data on the client.
                        });
                 })
             )

## Accessing an Existing AutoComplete

You can reference an existing AutoComplete instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/autocomplete/methods.aspx) to control its behavior.

### Accessing an existing AutoComplete instance

    //Put this after your Kendo AutoComplete for ASP.NET MVC declaration
    <script>
    $(function() {
        // Notice that the Name() of the autocomplete is used to get its client-side instance
        var autocomplete = $("#productAutoComplete").data("kendoAutoComplete");
    });
    </script>


## Handling Kendo UI AutoComplete events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/autocomplete/events.aspx) exposed by Kendo UI autocomplete:

### WebForms - subscribe by handler name

    <%: Html.Kendo().AutoComplete()
        .Name("autocomplete")
        .BindTo(new string[] { "Item1", "Item2", "Item3" })
        .Events(e => e
            .Select("autocomplete_select")
            .Change("autocomplete_change")
        )
    %>
    <script>
        function autocomplete_select() {
            //Handle the select event
        }

        function autocomplete_change() {
            //Handle the change event
        }
    </script>


### Razor - subscribe by handler name

    @(Html.Kendo().AutoComplete()
      .Name("autocomplete")
      .BindTo(new string[] { "Item1", "Item2", "Item3" })
      .Events(e => e
            .Select("autocomplete_select")
            .Change("autocomplete_change")
      )
    )
    <script>
        function autocomplete_select() {
            //Handle the select event
        }

        function autocomplete_change() {
            //Handle the change event
        }
    </script>


### Razor - subscribe by template delegate

    @(Html.Kendo().AutoComplete()
      .Name("autocomplete")
      .BindTo(new string[] { "Item1", "Item2", "Item3" })
      .Events(e => e
          .Select(@<text>
            function() {
                //Handle the select event inline
            }
          </text>)
          .Change(@<text>
            function() {
                //Handle the change event inline
            }
            </text>)
      )
    )

