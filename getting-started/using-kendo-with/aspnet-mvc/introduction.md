---
title: Introduction
slug: mvc-introduction
publish: true
---

## What is ASP.NET MVC

 [ASP.NET MVC](http://www.asp.net/mvc/) is a free and fully supported Microsoft framework for building web applications that use the model-view-controller pattern.
ASP.NET MVC is built on top of the [ASP.NET](http://www.asp.net/) framework.

## What is Kendo UI Complete for ASP.NET MVC

Kendo UI Complete for ASP.NET MVC is a set of HTML helpers which help you configure Kendo UI widgets by using server-side code in ASP.NET MVC applications.

Kendo UI Complete for ASP.NET MVC provides the following benefits:

*   Built on top of the Kendo UI HTML5 framework and jQuery
*   Leverages ASP.NET MVC features - data annotation, editor and display templates, validation, authorization
*   Supports the WebForms and Razor view engines

## Downloading and Installing Kendo UI Complete for ASP.NET MVC

You can choose to download either the msi installer or the zip file. If you choose the former just run the msi file to install it. If you choose to
download the zip file simply extract it to your preferred location.

The distribution files contain the following:

*   **\js** - Kendo UI minified JavaScript files
*   **\styles** - Kendo UI minified CSS files
*   **\wrappers\aspnetmvc\Binaries** - Kendo UI Complete for ASP.NET MVC assemblies
*   **\wrappers\aspnetmvc\Examples** - a sample ASP.NET MVC application
*   **\wrappers\aspnetmvc\EditorTemplates** - ready-to-use editor templates based on various Kendo UI widgets
*   **\wrappers\aspnermvc\LegacyThemes** - Kendo UI themes ported from [Telerik Extensions for ASP.NET MVC](http://www.telerik.com/products/aspnet-mvc.aspx) themes

## Getting Started with Kendo UI Complete for ASP.NET MVC

Follow these steps:

1.  Create a new ASP.NET MVC application from Visual Studio. ASP.NET MVC 3 and 4 are supported.

2.  Add a reference to **\wrappers\aspnetmvc\Binaries\Mvc3\Kendo.Mvc.dll**

3.  Copy the Kendo UI JavaScript files from **\js** to the **Scripts** folder of your application.

4.  Copy the Kendo UI CSS files from **\styles** to the **Content** folder of your application.

5.  Configure your ASP.NET MVC layout page to use the Kendo UI scripts and themes:
    * For Kendo UI Web (WebForms)

             <link href="<%= Url.Content("~/Content/kendo.common.min.css") %>" rel="stylesheet" type="text/css" />
             <link href="<%= Url.Content("~/Content/kendo.default.min.css") %>" rel="stylesheet" type="text/css" />
             <script src="<%= Url.Content("~/Scripts/jquery.min.js") %>"></script>
             <script src="<%= Url.Content("~/Scripts/kendo.web.min.js") %>"></script>
             <script src="<%= Url.Content("~/Scripts/kendo.aspnetmvc.min.js") %>"></script>
    * For Kendo UI Web (Razor)

             <link rel="stylesheet" href="@Url.Content("~/Content/kendo.common.min.css")">
             <link rel="stylesheet" href="@Url.Content("~/Content/kendo.default.min.css")">
             <script src="@Url.Content("~/Scripts/jquery.min.js")"></script>
             <script src="@Url.Content("~/Scripts/kendo.web.min.js")"></script>
             <script src="@Url.Content("~/Scripts/kendo.aspnetmvc.min.js")"></script>
    * Kendo UI DataViz (WebForms)

             <link href="<%= Url.Content("~/Content/kendo.dataviz.min.css") %>" rel="stylesheet" type="text/css" />
             <script src="<%= Url.Content("~/Scripts/jquery.min.js") %>"></script>
             <script src="<%= Url.Content("~/Scripts/kendo.dataviz.min.js") %>"></script>
             <script src="<%= Url.Content("~/Scripts/kendo.aspnetmvc.min.js") %>"></script>
    * Kendo UI DataViz (Razor)

             <link href="@Url.Content("~/Content/kendo.dataviz.min.css")" rel="stylesheet" type="text/css" />
             <script src="@Url.Content("~/Scripts/jquery.min.js")"></script>
             <script src="@Url.Content("~/Scripts/kendo.dataviz.min.js")"></script>
             <script src="@Url.Content("~/Scripts/kendo.aspnetmvc.min.js")"></script>
> You can also include the JavaScript and CSS files from CDN (specify the version e.g. 2012.2.710)

             <link href="http://cdn.kendostatic.com/<version>/styles/kendo.common.min.css" rel="stylesheet" type="text/css" />
             <link href="http://cdn.kendostatic.com/<version>/styles/kendo.default.min.css" rel="stylesheet" type="text/css" />
             <!-- jQuery is not hosted on Kendo CDN - include from another location -->
             <script src="http://code.jquery.com/jquery-1.7.1.min.js"></script>
             <script src="http://cdn.kendostatic.com/<version>/js/kendo.web.min.js"></script>
             <script src="http://cdn.kendostatic.com/<version>/js/kendo.aspnetmvc.min.js"></script>

6. Add a reference to the **Kendo.Mvc.UI** namespace to the **web.config**. Then the `Kendo` HtmlHelper extension would
be availble in your views.
    * If you are using the WebForms view engine open the **web.config** file in the root folder of your application. Add
     `<add namespace="Kendo.Mvc.UI" />` before the closing `namespaces` tag:

             <namespaces>
                 <add namespace="System.Web.Mvc" />
                 <add namespace="System.Web.Mvc.Ajax" />
                 <add namespace="System.Web.Mvc.Html" />
                 <add namespace="System.Web.Routing" />
                 <add namespace="System.Linq" />
                 <add namespace="System.Collections.Generic" />
                 <add namespace="Kendo.Mvc.UI" />
             </namespaces>
    * If you are using the Razor view engine open the **web.config** file which is in the **Views** folder
     of your application.Add `<add namespace="Kendo.Mvc.UI" />` before the closing `namespaces` tag:

             <system.web.webPages.razor>
                 <pages pageBaseType="System.Web.Mvc.WebViewPage">
                     <namespaces>
                         <add namespace="System.Web.Mvc" />
                         <add namespace="System.Web.Mvc.Ajax" />
                         <add namespace="System.Web.Mvc.Html" />
                         <add namespace="System.Web.Routing" />
                         <add namespace="Kendo.Mvc.UI" />
                     </namespaces>
                 </pages>
             </system.web.webPages.razor>

7. In case **ASP.NET MVC 4** is used, a **binding redirect** should be added to the root **web.config** file:

        <configuration>
          <!--... elements deleted for clarity ...-->

          <runtime>
            <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
              <dependentAssembly>
                <assemblyIdentity name="System.Web.Helpers"
                     publicKeyToken="31bf3856ad364e35" />
                <bindingRedirect oldVersion="1.0.0.0" newVersion="2.0.0.0"/>
              </dependentAssembly>
              <dependentAssembly>
                <assemblyIdentity name="System.Web.Mvc"
                     publicKeyToken="31bf3856ad364e35" />
                <bindingRedirect oldVersion="1.0.0.0-3.0.0.0" newVersion="4.0.0.0"/>
              </dependentAssembly>
              <dependentAssembly>
                <assemblyIdentity name="System.Web.WebPages"
                     publicKeyToken="31bf3856ad364e35" />
                <bindingRedirect oldVersion="1.0.0.0" newVersion="2.0.0.0"/>
              </dependentAssembly>
            </assemblyBinding>
          </runtime>
        </configuration>

8.  Use any Kendo UI HtmlHelper extension:
    * WebForms

            <%: Html.Kendo().DatePicker().Name("Birthday") %>
    * Razor

            @(Html.Kendo().DatePicker().Name("Birthday"))

## Running the sample application

You can find a sample ASP.NET MVC application in the **\wrappers\aspnetmvc\Examples** folder.
It contains the following:

*   **Areas/aspx** - WebForm views
*   **Areas/razor** - Razor views
*   **Controllers** - controller classes
*   **Models** - model classes
