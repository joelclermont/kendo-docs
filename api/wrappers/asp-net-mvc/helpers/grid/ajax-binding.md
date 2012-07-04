---
title: Ajax Binding
slug: mvc-grid-ajax-binding
publish: true
---

# Ajax Binding

## Getting started

When configured for ajax binding the Kendo Grid for ASP.NET MVC will make ajax requests when doing paging, sorting, filtering or grouping.

To configure the Kendo Grid for ajax binding follow these steps:

1.  Add a new action method which will return data to populate the grid:

        public ActionResult Products_Read()
        {
            var products = new NorthwindDataContext().Products;
        }
2.  Add a new parameter of type `Kendo.UI.DataSourceRequest`.
It will contain the current grid request information - page, sort, group and filter.
Decorate that parameter with the `Kendo.UI.DataSourceRequestAttribute`. That attribute is responsible for populating the `DataSourceRequest` object.

        public ActionResult Products_Read([DataSourceRequest]DataSourceRequest request)
        {
            var products = new NorthwindDataContext().Products;
        }
3.  Use the `ToDataSourceResult` extension method to convert your `IQueryable` or `IEnumerable` to a
`Kendo.UI.DataSourceResult` object. That extension method will page, filter, sort or group your data using the information provided by the
`DataSourceRequest` object. To use the `ToDataSourceResult` extension method import the `Kendo.Mvc.Extensions` namespace.

        public ActionResult Products_Read([DataSourceRequest]DataSourceRequest request)
        {
            var products = new NorthwindDataContext().Products;

            DataSourceResult result = products.ToDataSourceResult(request);
        }
4.  Return the `DataSourceResult` as JSON:

        public ActionResult Products_Read([DataSourceRequest]DataSourceRequest request)
        {
            var products = new NorthwindDataContext().Products;

            DataSourceResult result = products.ToDataSourceResult(request);

            return Json(result);
        }
5.  In the view configure the grid to use the action method created in the previous steps:
    - WebForms

            <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Grid")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductID);
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice);
                    columns.Bound(p => p.UnitsInStock);
                })
                .DataSource(dataSource => dataSource
                    .Ajax() // Specify that the data source is of ajax type
                    .Read(read => read.Action("Products_Read", "Home")) // Specify the action method and controller name
                )
                .Pageable()
            %>
    - Razor

            @(Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Grid")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductID);
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice);
                    columns.Bound(p => p.UnitsInStock);
                })
                .DataSource(dataSource => dataSource
                    .Ajax() // Specify that the data source is of ajax type
                    .Read(read => read.Action("Products_Read", "Home")) // Specify the action method and controller name
                )
                .Pageable()
            )


The `ToDataSourceResult` method uses the `DataSourceRequest` parameter and Linq expressions to apply paging, sorting, filtering and grouping.
The JSON response of the action method will contain only a single page of data. The grid will be bound to that data.

## Pass Additional Data to Action Method

To pass additional parameters to the action method use the `Data` setting. Provide the name of a JavaScript function which will return an object
containing the additional data:



### Action method

    public ActionResult Products_Read([DataSourceRequest]DataSourceRequest request, string firstName, string lastName)
    {
        //Implementation omitted
    }


### WebForms - Send additional data

    <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
        .Name("Grid")
        .DataSource(dataSource => dataSource
            .Ajax()
            .Read(read => read.Action("Products_Read", "Home")
                      .Data("additionalData") // the name of the JavaScript function which will return the additional data
            )
        )
        .Pageable()
    %>
    <script>
    function additionalData() {
        return {
            firstName: "John",
            lastName: "Doe"
        };
    }
    </script>


### Razor - Send additional data

    @(Html.Kendo().Grid<MvcApplication1.Models.Product>()
        .Name("Grid")
        .DataSource(dataSource => dataSource
            .Ajax()
            .Read(read => read.Action("Products_Read", "Home")
                .Data("additionalData") // the name of the JavaScript function which will return the additional data
            )
        )
        .Pageable()
    )
    <script>
    function additionalData() {
        return {
            firstName: "John",
            lastName: "Doe"
        };
    }
    </script>


## Enable Client Data Processing during Ajax Binding

By default Kendo Grid for ASP.NET MVC will request data from the server every time the user changes the page, filters the grid, sorts or groups. This behavior
can be changed by disabling `ServerOperation`:

    .DataSource(dataSource => dataSource
        .Ajax()
        .ServerOperation(false) // paging, sorting, filtering and grouping will be applied client-side
        .Read(read => read.Action("Products_Read", "Home"))
    )
