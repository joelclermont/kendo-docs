---
title: MVC Grid Batch Editing
slug: mvc-grid-batch-editing
publish: true
---

# Cell Editing and Batch Updates

## Getting started

Cell editing mode allows the user to edit data in a way similar to popular spreadsheet programs - double clicking a cell puts it in edit mode.
Clicking outside the cell accepts the new value. All modified grid records are updated (saved, inserted or deleted) when the "Save changes" button is clicked.

To enable this mode follow these steps:

1.  Set the edit mode to `InCell`:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Grid")
                // Set the edit mode
                .Editable(editing => editing.Mode(GridEditMode.InCell))
        %>
2.  Add `Create` and `Save` commands:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Grid")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => command.Destroy()).Width(110);
                })
                .Editable(editing => editing.Mode(GridEditMode.InCell))
                // Command configuration -->
                .ToolBar(toolbar =>
                {
                    toolbar.Create();
                    toolbar.Save();
                })
                // <-- Command configuration
        %>
3.  Specify the action methods which will handle the `Create`, `Update` and `Destroy` operations:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Grid")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => command.Destroy()).Width(110);
                })
                .Editable(editing => editing.Mode(GridEditMode.InCell))
                .ToolBar(toolbar =>
                {
                    toolbar.Create();
                    toolbar.Save();
                })
                .DataSource(dataSource => dataSource
                    .Ajax()
                    // CRUD configuration -->
                    .Create(create => create.Action("Products_Create", "Home"))
                    .Read(read => read.Action("Products_Read", "Home"))
                    .Update(update => update.Action("Products_Update", "Home"))
                    .Destroy(destroy => destroy.Action("Products_Destroy", "Home"))
                    // <-- CRUD configuration
                )
        %>
4.  Specify the property of the model which is the unique identifier (primary key):

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Grid")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => command.Destroy()).Width(110);
                })
                .Editable(editing => editing.Mode(GridEditMode.InCell))
                .ToolBar(toolbar =>
                {
                    toolbar.Create();
                    toolbar.Save();
                })
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
5.  Enable batch mode:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Grid")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => command.Destroy()).Width(110);
                })
                .Editable(editing => editing.Mode(GridEditMode.InCell))
                .ToolBar(toolbar =>
                {
                    toolbar.Create();
                    toolbar.Save();
                })
                .DataSource(dataSource => dataSource
                    .Ajax()
                    .Model(model => model.Id(p => p.ProductID))
                    // Enable batch mode
                    .Batch(true)
                    .Create(create => create.Action("Products_Create", "Home"))
                    .Read(read => read.Action("Products_Read", "Home"))
                    .Update(update => update.Action("Products_Update", "Home"))
                    .Destroy(destroy => destroy.Action("Products_Destroy", "Home"))
                )
        %>
6.  Implement the `Read` action method.

        public ActionResult Products_Read([DataSourceRequest] DataSourceRequest request)
        {
            return Json(ProductRepository.All().ToDataSourceResult(request));
        }
7.  Implement the `Create` action method:

        [AcceptVerbs(HttpVerbs.Post)]
        public ActionResult Products_Create([DataSourceRequest] DataSourceRequest request, [Bind(Prefix = "models")]IEnumerable<Product> products)
        {
            var results = new List<Product>();

            if (products != null &amp;&amp; ModelState.IsValid)
            {
                foreach (var product in products)
                {
                    ProductRepository.Insert(product);
                    results.Add(product);
                }
            }

            // Return the newly created products and the ModelState (in case there are any validation errors)
            return Json(result.ToDataSourceResult(request, ModelState));
        }
8.  Implement the `Update` action method:

        [AcceptVerbs(HttpVerbs.Post)]
        public ActionResult Products_Update([DataSourceRequest] DataSourceRequest request, [Bind(Prefix = "models")]IEnumerable<Product> products)
        {
            if (products != null &amp;&amp; ModelState.IsValid)
            {
                foreach (var product in products)
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
            }

            // Return the ModelState in case there are any validation errors
            return Json(ModelState.ToDataSourceResult());
        }
9.  Implement the `Destroy` action method:

        [AcceptVerbs(HttpVerbs.Post)]
        public ActionResult Products_Destroy([DataSourceRequest] DataSourceRequest request, [Bind(Prefix = "models")]IEnumerable<product> products)
        {
            if (products.Any())
            {
                foreach (var product in products)
                {
                    ProductRepository.Delete(product);
                }
            }

            // Return the ModelState in case there are any validation errors
            return Json(ModelState.ToDataSourceResult());
        }
10.  Show any validation errors by handling the `Error` event of the `DataSource`:

        <%: Html.Kendo().Grid<MvcApplication1.Models.Product>()
                .Name("Grid")
                .Columns(columns =>
                {
                    columns.Bound(p => p.ProductName);
                    columns.Bound(p => p.UnitPrice).Width(140);
                    columns.Bound(p => p.UnitsInStock).Width(140);
                    columns.Bound(p => p.Discontinued).Width(100);
                    columns.Command(command => command.Destroy()).Width(110);
                })
                .Editable(editing => editing.Mode(GridEditMode.InCell))
                .ToolBar(toolbar =>
                {
                    toolbar.Create();
                    toolbar.Save();
                })
                .DataSource(dataSource => dataSource
                    .Ajax()
                    .Model(model => model.Id(p => p.ProductID))
                    // Specify a handler for the error event
                    .Events(events => events.Error("error"))
                    .Batch(true)
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

