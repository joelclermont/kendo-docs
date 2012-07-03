---
title: MVC Grid Configuration
slug: mvc-grid-configuration
publish: true
---

## Common DataSource Settings

The `DataSource` of the Kendo Grid for ASP.NET MVC contains configuration used by
the [Kendo DataSource](http://www.kendoui.com/documentation/framework/datasource/overview.aspx) object.

Kendo Grid for ASP.NET MVC supports two types of data sources -
[server](http://www.kendoui.com/documentation/asp-net-mvc/helpers/grid/server-binding.aspx) and
[ajax](http://www.kendoui.com/documentation/asp-net-mvc/helpers/grid/ajax-binding.aspx).

###  Aggregates

Sets the aggregates.

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Aggregates(aggregates =>
        {
            aggregates.Add(p => p.UnitsInStock).Min().Max().Count();
            aggregates.Add(p => p.UnitsOnOrder).Average();
            aggregates.Add(p => p.ProductName).Count();
            aggregates.Add(p => p.UnitPrice).Sum();
        })
    )

###   Create
Specify the action method which will create new model

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Create(create => create.Action(/### action ###/ "Create", /### controller ###/ "Home"))
    )
###   Destroy
Specify the action method which will destroy existing models.

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Destroy(destroy =>  destroy.Destroy(/### action ###/ "Destroy", /### controller ###/ "Home"))
    )
###   Events
Handle the [events](http://www.kendoui.com/documentation/framework/datasource/events.aspx) of the Kendo DataSource object.

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Events(events => events
            // Subscribe to the "change" event. The name of the JavaScript function which will be invoked is "changeHandler".
            .Change("changeHandler")
            // Subscribe to the "error" event. The name of the JavaScript function which will be invoked is "errorHandler".
            .Error("errorHandler")
            // Subscribe to the "requestStart" event. The name of the JavaScript function which will be invoked is "requestStartHandler".
            .RequestStart("requestStartHandler")
        )
    )
###   Filter
Set the initial filter.

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Filter(filters =>
        {
            // Show products whose ProductName property contains "C"
            filters.Add(p => p.ProductName).Contains("C");
            // and UnitsInStock is greater than 10
            filters.Add(p => p.UnitsInStock).IsGreaterThan(10);
        })
    )
###   Group
Set the initial grouping.

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Groups(groups =>
        {
            // Group by the UnitPrice property
            groups.Add(p => p.UnitPrice);
            // Then by ProductName property
            groups.Add(p => p.ProductName);
        })
    )
###   Model
Configure the model of the data source.

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Model(model =>
        {
            //The unique identifier (primary key) of the model is the ProductID property
            model.Id(p => p.ProductID);

            // Declare a model field and optionally specify its default value (used when a new model instance is created)
            model.Field(p => p.ProductName).DefaultValue("N/A");

            // Declare a model field and make it readonly
            model.Field(p => p.UnitPrice).Editable(false);
        })
    )
###   PageSize
Set the page size used during paging. The default page size is 10.

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .PageSize(20)
    )
###   Read
Specify the action method which will read existing models and return them as JSON:

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Read(read =>  read.Read(/### action ###/ "Read", /### controller ###/ "Home"))
    )
###   Sort
Set the initial sort.

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Sort(sort =>
        {
            // Sort by UnitsInStock in descending order
            sort.Add(p => p.UnitsInStock).Descending();
            // then by ProductName in ascending order
            sort.Add(p => p.ProductName);
        })
    )

###   Update
Specify the action method which will update existing models:

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
        .Update(update =>  update.Update(/### action ###/ "Update", /### controller ###/ "Home"))
    )

## Ajax DataSource Settings

To configure a `DataSource` to use ajax binding use the `Ajax` method:

    .DataSource(dataSource => dataSource
        .Ajax() // or .Server()
    )


###  Batch

Enable or disable batch create, update and destroy operations. By default batch operations are disabled.

    .DataSource(dataSource => dataSource
        .Ajax()
        // Enable batch operations
        .Batch(true)
    )

## Server DataSource Configuration

To configure a `DataSource` to use server binding use the `Server` method:

    .DataSource(dataSource => dataSource
        .Server()
    )

## Column Configuration

To add grid columns use the `Columns` method:

### WebForms

    <% Html.Kendo().Grid<MvcApplication1.Models.Product>()
       .Name("Grid")
       // Column configuration -->
       .Columns(columns =>
       {
           // Define a column which will display the value of the ProductID property
           columns.Bound(p => p.ProductID);

           // Define a column and set a column setting
           columns.Bound(p => p.ProductName).Title("Product Name");

           // Define a template column - it needs a server side code block <% %>
           columns.Template(p =>
           {
                %>
                    <%: Html.ActionLink("Edit", "Home", new { id = p.ProductID }) %>
                <%
           });

           // Define a command column with a "Destroy" button

           columns.Command(commands =>
           {
                commands.Destroy();
           });
       })
       // The Render method is used because of the server side code blocks
       .Render();
    %>

### Razor

    @( Html.Kendo().Grid<MvcApplication1.Models.Product>()
       .Name("Grid")
       // Column configuration -->
       .Columns(columns =>
       {
           // Define a column which will display the value of the ProductID property
           columns.Bound(p => p.ProductID);

           // Define a column and set a column setting
           columns.Bound(p => p.ProductName).Title("Product Name");

           // Define a template column - it needs a templated razor delegate
           columns.Template(@<text>
                @Html.ActionLink("Edit", "Home", new { id = p.ProductID })
           </text>);

           // Define a command column with a "Destroy" button

           columns.Command(commands =>
           {
                commands.Destroy();
           });
       })
    )


## Bound Column Settings

A bound column is declared via the `Bound` method. It has the following settings:

###   ClientTemplate
A [Kendo template](http://www.kendoui.com/documentation/framework/templates/overview.aspx)
which specifies the way the column is displayed. Works **only** when the grid is configured for
[ajax binding](http://www.kendoui.com/documentation/asp-net-mvc/helpers/grid/ajax-binding.aspx).

    // Display the ProductName inside a strong tag
    columns.Bound(p => p.ProductName).ClientTemplate("<strong>#: ProductName #</strong>");
###   Encoded
Enables or disables the HTML encoding of the bound property value. By default is set to `true` which means that
column values are encoded.

    // Stop encoding the value of the bound field
    columns.Bound(p => p.ProductName).Encoded(false);
###   Filterable
Enables or disables the filtering UI. By default set to `true` which means that bound grid columns can be filtered using
the filtering UI.

    // Disable filtering
    columns.Bound(p => p.ProductID).Filterable(false);
###   Format
Specifies the format used when displaying the value of the bound property. Empty by default.

    // Format the value as currency
    columns.Bound(p => p.UnitPrice).Format("{0:C}");

The available formats are described in the [Globalization](http://www.kendoui.com/documentation/framework/globalization/overview.aspx)
help topic.

###   Groupable
Enables or disables dragging the column header to group by its bound property. By default set to `true` which means that bound
grid columns can be dragged for grouping.

    // Disable grouping
    columns.Bound(p => p.ProductID).Groupable(false);
###   Sortable
Enables or disables sorting by that column.
// Disable grouping
columns.Bound(p =&gt; p.ProductID).Sortable(false);

###   Template
Sets the server template which will be used when displaying the bound field.  Works **only**
when the grid is configured for [server binding](http://www.kendoui.com/documentation/asp-net-mvc/helpers/grid/server-binding.aspx).
Template syntax is different for WebForms and Razor views. In WebForms the template is a [server side code block](http://msdn.microsoft.com/en-us/library/ms178135%28vs.80%29.aspx).
In Razor the template is a [templated razor delegate](http://haacked.com/archive/2011/02/27/templated-razor-delegates.aspx).

#### WebForms

    <% Html.Kendo.Grid(Model)
       .Columns(columns =>
       {
            // Template is a server side code block <% %>
            columns.Bound(p => p.ProductID).Template(p =>
            {
                %>
                    <strong><%: p.ProductID %></strong>
                <%
            });
       })
       // The Render method is used because of the server side code blocks
       .Render();
    %>

#### Razor

    @( Html.Kendo.Grid(Model)
       .Columns(columns =>
       {
            // Template is a templated razor delegate - the argument of the delegate is called "item"
            columns.Bound(p => p.ProductID).Template(@<text>
                <strong>@item.ProductID</strong>
            </text>);
       })
    )
         ###   `Title`: sets the text displayed in the header of the column. By default the property name is used as title.

    // Set the column title
    columns.Bound(p => p.ProductID).Title("Title");
        ###   `Width`: sets the width of the column in pixels or other units. By default the width is not set and the column would try to accomodate its content.

    // Set the column width in pixels
    columns.Bound(p => p.ProductID).Width(200);
    // Set the column width in em
    columns.Bound(p => p.ProductID).Width("10em");


## Template Column Settings

A template column is declared via the `Template` method. It has the following settings:

###   ClientTemplate
A [Kendo template](http://www.kendoui.com/documentation/framework/templates/overview.aspx)
which specifies the way the column is displayed. Works **only** when the grid is configured for [ajax binding](http://www.kendoui.com/documentation/asp-net-mvc/helpers/grid/ajax-binding.aspx).

###   Title
Sets the text displayed in the header of the column. Empty by default.

###   Width
Sets the width of the column in pixels or other units. By default the width is not set and the column would try to accomodate its content.
