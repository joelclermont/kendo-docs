---
title: Overview
publish: true
---

# Menu

The Menu HtmlHelper extension is a server-side wrapper for the [Kendo UI Menu](http://www.kendoui.com/documentation/ui-widgets/menu/overview.aspx) widget.

## Getting Started

There are several ways to define items of the Kendo Menu for ASP.NET MVC

*   use items builder - manually define the properties of each Menu item.
*   sitemap binding - uses a sitemap to create the items of the Menu.
*   model binding - uses a collection of objects to create the items of the Menu.

### Define items of the Kendo Menu

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

        public ActionResult Index()
        {
            return View();
        }
3.  Add a simple menu:
    - WebForms

            <%: Html.Kendo().Menu()
                    .Name("menu") //The name of the menu is mandatory. It specifies the "id" attribute of the widget.
                    .Items(items =>
                    {
                        items.Add().Text("Item 1"); //Add item with text "Item1")
                        items.Add().Text("Item 2"); //Add item with text "Item2")
                    })
            %>
    - Razor

            @(Html.Kendo().Menu()
                .Name("menu") //The name of the menu is mandatory. It specifies the "id" attribute of the widget.
                .Items(items =>
                {
                    items.Add().Text("Item 1"); //Add item with text "Item1")
                    items.Add().Text("Item 2"); //Add item with text "Item2")
                })
            )

### Bind Kendo Menu to a sitemap

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a simple sitemap with **sample.sitemap** file name at the root of the project:

        <?xml version="1.0" encoding="utf-8" ?>
        <siteMap>
          <siteMapNode title="Home" controller="Home" action="Overview">
            <siteMapNode title="Grid">
              <siteMapNode controller="grid" action="index" title="First Look (Razor)" area="razor"/>
              <siteMapNode controller="grid" action="index" title="First Look (ASPX)" area="aspx"/>
            </siteMapNode>
            <siteMapNode title="Menu">
              <siteMapNode controller="menu" action="index" title="First Look (Razor)" area="razor"/>
              <siteMapNode controller="menu" action="index" title="First Look (ASPX)" area="aspx"/>
            </siteMapNode>
          </siteMapNode>
        </siteMap>
3.  Load the sitemap using SiteMapManager:

        public ActionResult Index()
        {
            if (!SiteMapManager.SiteMaps.ContainsKey("sample"))
            {
                SiteMapManager.SiteMaps.Register<xmlsitemap>("sample", sitmap => sitmap.LoadFrom("~/sample.sitemap"));
            }
            return View();
        }
4.  Add a menu:
    - WebForms

            <%: Html.Kendo().Menu()
                    .Name("menu") //The name of the menu is mandatory. It specifies the "id" attribute of the widget.
                    .BindTo("sample") //bind to sitemap with name "sample"
            %>
    - Razor

            @(Html.Kendo().Menu()
                  .Name("menu") //The name of the menu is mandatory. It specifies the "id" attribute of the widget.
                  .BindTo("sample") //bind to sitemap with name "sample"
            )

### Bind Kendo Menu to a hierarchical model

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method and pass the Categories table as the model. Note that the Categories should have association to the Products table:

        public ActionResult Index()
        {
            NorthwindDataContext northwind = new NorthwindDataContext();

            return View(northwind.Categories);
        }
3.  Make your view strongly typed:
    - WebForms

            <%@ Page Language="C#" MasterPageFile="~/Views/Shared/Site.Master"
                Inherits="System.Web.Mvc.ViewPage<IEnumerable<MvcApplication1.Models.Category>>" %>
    - Razor

            @model IEnumerable<MvcApplication1.Models.Category>
4.  Add a menu:
    - WebForms

            <%: Html.Kendo().Menu()
                    .Name("menu") //The name of the menu is mandatory. It specifies the "id" attribute of the widget.
                    .BindTo(Model, mappings =>
                    {
                        mappings.For<category>(binding => binding //define first level of menu
                            .ItemDataBound((item, category) => //define mapping between menu item properties and the model properties
                            {
                                item.Text = category.CategoryName;
                            })
                            .Children(category => category.Products)); //define which property of the model contains the children
                        mappings.For<product>(binding => binding
                            .ItemDataBound((item, product) =>
                            {
                                item.Text = product.ProductName;
                            }));
                    })
            %>
    - Razor

            @(Html.Kendo().Menu()
                  .Name("menu") //The name of the menu is mandatory. It specifies the "id" attribute of the widget.
                  .BindTo(Model, mappings =>
                  {
                      mappings.For<category>(binding => binding //define first level of menu
                          .ItemDataBound((item, category) => //define mapping between menu item properties and the model properties
                              {
                              item.Text = category.CategoryName;
                              })
                          .Children(category => category.Products)); //define which property of the model contains the children
                      mappings.For<product>(binding => binding
                          .ItemDataBound((item, product) =>
                          {
                              item.Text = product.ProductName;
                          }));
                })
            )

## Accessing an Existing Menu

You can reference an existing Menu instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/menu/methods.aspx) to control its behavior.


### Accessing an existing Menu instance

    //Put this after your Kendo Menu for ASP.NET MVC declaration
    <script>
    $(function() {
        // Notice that the Name() of the menu is used to get its client-side instance
        var menu = $("#menu").data("kendoMenu");
    });
    </script>


## Handling Kendo UI Menu events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/menu/events.aspx) exposed by Kendo UI Menu:

### WebForms - subscribe by handler name

    <%: Html.Kendo().Menu()
            .Name("menu")
            .Events(e => e
                .Open("menu_open")
                .Close("menu_close")
            )
    %>
    <script>
    function menu_close() {
        //Handle the close event
    }

    function menu_open() {
        //Handle the open event
    }
    </script>


### Razor - subscribe by handler name

    @(Html.Kendo().Menu()
          .Name("menu")
          .Events(e => e
                .Open("menu_open")
                .Close("menu_close")
          )
    )
    <script>
    function menu_close() {
        //Handle the close event
    }

    function menu_open() {
        //Handle the open event
    }
    </script>


### Razor - subscribe by template delegate

    @(Html.Kendo().Menu()
          .Name("menu")
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

