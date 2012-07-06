---
title: Overview
slug: mvc-tabstrip-overview
publish: true
---

# TabStrip

The TabStrip HtmlHelper extension is a server-side wrapper for the [Kendo UI TabStrip](http://www.kendoui.com/documentation/ui-widgets/tabstrip/overview.aspx) widget.

## Getting Started

There are several ways to define items of the Kendo TabStrip for ASP.NET MVC

*   use items builder - manually define the properties of each TabStrip item.
*   sitemap binding - uses a sitemap to create the items of the TabStrip.
*   model binding - uses a collection of objects to create the items of the TabStrip.

### Define items of the Kendo TabStrip

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

        public ActionResult Index()
        {
            return View();
        }
3.  Add a simple tabstrip:
    - WebForms

            <%: Html.Kendo().TabStrip()
                    .Name("tabstrip") //The name of the tabstrip is mandatory. It specifies the "id" attribute of the widget.
                    .Items(items =>
                    {
                        items.Add().Text("Item 1"); //Add item with text "Item1")
                        items.Add().Text("Item 2"); //Add item with text "Item2")
                    })
            %>
    - Razor

            @(Html.Kendo().TabStrip()
                .Name("tabstrip") //The name of the tabstrip is mandatory. It specifies the "id" attribute of the widget.
                .Items(items =>
                {
                    items.Add().Text("Item 1"); //Add item with text "Item1")
                    items.Add().Text("Item 2"); //Add item with text "Item2")
                })
            )

### Bind Kendo TabStrip to a sitemap

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a simple sitemap with **sample.sitemap** file name at the root of the project:

        <?xml version="1.0" encoding="utf-8" ?>
        <siteMap>
          <siteMapNode title="Home" controller="Home" action="Overview">
          <siteMapNode controller="grid" action="index" title="Grid" />
          <siteMapNode controller="tabstrip" action="index" title="TabStrip" />
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
4.  Add a tabstrip:
    - WebForms

            <%: Html.Kendo().TabStrip()
                    .Name("tabstrip") //The name of the tabstrip is mandatory. It specifies the "id" attribute of the widget.
                    .BindTo("sample") //bind to sitemap with name "sample"
            %>
    - Razor

            @(Html.Kendo().TabStrip()
                .Name("tabstrip") //The name of the tabstrip is mandatory. It specifies the "id" attribute of the widget.
                .BindTo("sample") //bind to sitemap with name "sample"
            )

### Bind Kendo TabStrip to a model

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method and pass the Categories table as the model:

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
4.  Add a tabstrip:
    - WebForms

            <%: Html.Kendo().TabStrip()
                    .Name("tabstrip") //The name of the tabstrip is mandatory. It specifies the "id" attribute of the widget.
                    .BindTo(item, Model =>
                    {
                        item.Text = category.CategoryName;
                    })
            %>
    - Razor

            @(Html.Kendo().TabStrip()
                  .BindTo(item, Model =>
                  {
                     item.Text = category.CategoryName;
                  })
            )

## Accessing an Existing TabStrip

You can reference an existing TabStrip instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/tabstrip/methods.aspx) to control its behavior.

### Accessing an existing TabStrip instance

    //Put this after your Kendo TabStrip for ASP.NET MVC declaration
    <script>
    $(function() {
        // Notice that the Name() of the tabstrip is used to get its client-side instance
        var tabstrip = $("#tabstrip").data("kendoTabStrip");
    });
    </script>

## Handling Kendo UI TabStrip events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/tabstrip/events.aspx) exposed by Kendo UI TabStrip:

### WebForms - subscribe by handler name

    <%: Html.Kendo().TabStrip()
            .Name("tabstrip")
            .Events(e => e
                .Select("tabstrip_select")
            )
    %>
    <script>
    function tabstrip_select() {
        //Handle the Select event
    }
    </script>


### Razor - subscribe by handler name

    @(Html.Kendo().TabStrip()
          .Name("tabstrip")
          .Events(e => e
                .Select("tabstrip_select")
          )
    )
    <script>
    function tabstrip_select() {
        //Handle the Select event
    }
    </script>


### Razor - subscribe by template delegate

    @(Html.Kendo().TabStrip()
          .Name("tabstrip")
          .Events(e => e
              .Select(@<text>
                function() {
                    //Handle the Select event inline
                }
              </text>)
          )
    )

