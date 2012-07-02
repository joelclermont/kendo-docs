---
title: Ajax Editing
publish: true
---

# Ajax Editing

## Getting started

To configure Kendo Grid for ASP.NET MVC for ajax editing follow these steps:

1.  Define a command column for the `Edit` and `Destroy` commands:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Home")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    // Add "Edit" and "Destroy" commands
                    columns.Command(command => { command.Edit(); command.Destroy(); }).Width(200);
                })
        %>
2.  Set the editing mode to `InLine`:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Home")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => { command.Edit(); command.Destroy(); }).Width(200);
                })
                // Set the edit mode to "InLine"
                .Editable(editable => editable.Mode(GridEditMode.InLine))
        %>
3.  Add the `Create` command to the grid toolbar:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Home")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => { command.Edit(); command.Destroy(); }).Width(200);
                })
                // Add "Create" command
                .ToolBar(commands => commands.Create())
                .Editable(editable => editable.Mode(GridEditMode.InLine))
        %>
4.  Specify the action methods which will handle the Create, Update and Destroy operations:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Home")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => { command.Edit(); command.Destroy(); }).Width(200);
                })
                .ToolBar(toolbar => toolbar.Create())
                .Editable(editable => editable.Mode(GridEditMode.InLine))
                .DataSource(dataSource => dataSource
                    .Ajax()
                    // Configure CRUD -->
                    .Create(create => create.Action("Products_Create", "Home"))
                    .Read(read => read.Action("Products_Read", "Home"))
                    .Update(update => update.Action("Products_Update", "Home"))
                    .Destroy(destroy => destroy.Action("Products_Destroy", "Home"))
                    // <-- Configure CRUD
                )
        %>
5.  Specify the property of the model which is the unique identifier (primary key):

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Home")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => { command.Edit(); command.Destroy(); }).Width(200);
                })
                .ToolBar(toolbar => toolbar.Create())
                .Editable(editable => editable.Mode(GridEditMode.InLine))
                .DataSource(dataSource => dataSource
                    .Ajax()
                    // Specify that the ProductID property is the unique identifier of the model
                    .Model(model => model.Id(p => p.ProductID))
                    .Create(create => create.Action("Products_Create", "Home"))
                    .Read(read => read.Action("Products_Read", "Home"))
                    .Update(update => update.Action("Products_Update", "Home"))
                    .Destroy(destroy => destroy.Action("Products_Destroy", "Home"))
                )
        %>
6.  Implement the `Read` action method:

        public ActionResult Products_Read([DataSourceRequest] DataSourceRequest request)
        {
            return Json(ProductRepository.All().ToDataSourceResult(request));
        }
7.  Implement the `Create` action method:

        [AcceptVerbs(HttpVerbs.Post)]
        public ActionResult Products_Create([DataSourceRequest] DataSourceRequest request, Product product)
        {
            if (product != null &amp;&amp; ModelState.IsValid)
            {
                ProductRepository.Insert(product);
            }

            //Return any validation errors if any
            return Json(new [] { product }.ToDataSourceResult(request, ModelState));
        }
8.  Implement the `Update` action method:

        [AcceptVerbs(HttpVerbs.Post)]
        public ActionResult Products_Update([DataSourceRequest] DataSourceRequest request, Product product)
        {
            if (product != null &amp;&amp; ModelState.IsValid)
            {
                var target = ProductRepository.One(p => p.ProductID == product.ProductID);
                if (target != null)
                {
                    target.ProductName = product.ProductName;
                    target.UnitPrice = product.UnitPrice;
                    target.UnitsInStock = product.UnitsInStock;
                    target.LastSupply = product.LastSupply;
                    target.Discontinued = product.Discontinued;
                    ProductRepository.Update(target);
                }
            }

            //Return any validation errors if any
            return Json(ModelState.ToDataSourceResult());
        }
9.  Implement the `Destroy` action method:

        [AcceptVerbs(HttpVerbs.Post)]
        public ActionResult Products_Destroy([DataSourceRequest] DataSourceRequest request, Product product)
        {
            if (product != null)
            {
                ProductRepository.Delete(product);
            }

            //Return any validation errors if any
            return Json(ModelState.ToDataSourceResult());
        }
10.  Show any validation errors by handling the Error event of the DataSource:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Home")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => { command.Edit(); command.Destroy(); }).Width(200);
                })
                .ToolBar(toolbar => toolbar.Create())
                .Editable(editable => editable.Mode(GridEditMode.InLine))
                .DataSource(dataSource => dataSource
                    .Ajax()
                    .Model(model => model.Id(p => p.ProductID))
                    // Specify a handler for the error event
                    .Events(events => events.Error("error"))
                    .Create(create => create.Action("Products_Create", "Home"))
                    .Read(read => read.Action("Products_Read", "Home"))
                    .Update(update => update.Action("Products_Update", "Home"))
                    .Destroy(destroy => destroy.Action("Products_Destroy", "Home"))
                )
        %>
        <script>
        function error(e) {
            if (e.errors) {
                var message = "Errors:\n";
                $.each(e.errors, function (key, value) {
                    if ('errors' in value) {
                        $.each(value.errors, function() {
                            message += this + "\n";
                        });
                    }
                });

                alert(message);
            }
        }
        </script>

