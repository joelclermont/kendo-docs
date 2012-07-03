---
title: Overview
publish: true
---

# Grid

The Grid HtmlHelper extension is a server-side wrapper for the [Kendo UI Grid](http://www.kendoui.com/documentation/ui-widgets/grid/overview.aspx) widget.

## Getting Started

There are two ways to bind a Kendo Grid for ASP.NET MVC:

*   [server ](http://www.kendoui.com/documentation/asp-net-mvc/helpers/grid/server-binding.aspx)- the grid will make HTTP GET requests when binding
*   [ajax ](http://www.kendoui.com/documentation/asp-net-mvc/helpers/grid/ajax-binding.aspx)- the grid will make ajax requests when binding

Here is how to configure the Kendo Grid for server binding to the Northwind Products table using Linq to SQL:

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
4.  Add a server bound grid:
    - WebForms

            <%: Html.Kendo().Grid(Model)         //The grid will be bound to the Model which is the Products table
                    .Name("productGrid") //The name of the grid is mandatory. It specifies the "id" attribute of the widget.
                    .Columns(columns =>
                    {
                        columns.Bound(p => p.ProductID);   //Create a column bound to the "ProductID" property
                        columns.Bound(p => p.ProductName); //Create a column bound to the "ProductName" property
                        columns.Bound(p => p.UnitPrice);   //Create a column bound to the "UnitPrice" property
                        columns.Bound(p => p.UnitsInStock);//Create a column bound to the "UnitsInStock" property
                    })
                    .Pageable() //Enable paging
            %>
    - Razor

        @(Html.Kendo().Grid(Model)            //The grid will be bound to the Model which is the Products table
              .Name("productGrid") //The name of the grid is mandatory. It specifies the "id" attribute of the widget.
              .Columns(columns =>
              {
                  columns.Bound(p => p.ProductID);   //Create a column bound to the "ProductID" property
                  columns.Bound(p => p.ProductName); //Create a column bound to the "ProductName" property
                  columns.Bound(p => p.UnitPrice);   //Create a column bound to the "UnitPrice" property
                  columns.Bound(p => p.UnitsInStock);//Create a column bound to the "UnitsInStock" property
              })
             .Pageable() //Enable paging
        )

## Accessing an Existing Grid

You can reference an existing Grid instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/grid/methods.aspx) to control its behavior.

### Accessing an existing Grid instance

    //Put this after your Kendo Grid for ASP.NET MVC declaration
    <script>
    $(function() {
        // Notice that the Name() of the grid is used to get its client-side instance
        var grid = $("#productGrid").data("kendoGrid");
    });
    </script>


## Handling Kendo UI Grid events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/grid/events.aspx) exposed by Kendo UI grid:


### WebForms - subscribe by handler name

    <%: Html.Kendo().Grid(Model)
            .Name("productGrid")
            .Events(e => e
                .DataBound("productGrid_dataBound")
                .Change("productGrid_change")
            )
    %>
    <script>
    function productGrid_dataBound() {
        //Handle the dataBound event
    }

    function productGrid_change() {
        //Handle the change event
    }
    </script>


### Razor - subscribe by handler name

    @(Html.Kendo().Grid(Model)
          .Name("productGrid")
          .Events(e => e
              .DataBound("productGrid_dataBound")
              .Change("productGrid_change")
          )
    )
    <script>
    function productGrid_dataBound() {
        //Handle the dataBound event
    }

    function productGrid_change() {
        //Handle the change event
    }
    </script>


### Razor - subscribe by template delegate

    @(Html.Kendo().Grid(Model)
          .Name("productGrid")
          .Events(e => e
              .DataBound(@<text>
                function() {
                    //Handle the dataBound event inline
                }
              </text>)
              .Change(@<text>
                function() {
                    //Handle the change event inline
                }
                </text>)
          )
    )
