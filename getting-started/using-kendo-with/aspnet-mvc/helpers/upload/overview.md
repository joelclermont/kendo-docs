---
title: Overview
slug: mvc-upload-overview
publish: true
---

# Upload

The Upload HtmlHelper extension is a server-side wrapper for the [Kendo UI Upload](http://www.kendoui.com/documentation/ui-widgets/upload/overview.aspx) widget.

## Getting Started

The following example shows how to setup an asynchronous upload that saves the uploaded files in the App_Data folder.:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

        public ActionResult Index()
        {
            return View();
        }

3.  Add the upload to the view:
    - WebForms

            <%: Html.Telerik().Upload()
                    .Name("attachments")
                    .Async(async => async
                        .Save("Save", "Home")
                    )
            %>

    - Razor

            @(Html.Telerik().Upload()
                    .Name("attachments")
                    .Async(async => async
                        .Save("Save", "Home")
                    )
            )

    The Name is used to specify the unique name of the Upload component. It is used to set the id and name HTML attributes.
    Setting the name is mandatory and exception would be thrown otherwise.

4. Implement the Save controller action:

        public ActionResult Save(IEnumerable<HttpPostedFileBase> attachments)
        {
            // The Name of the Upload component is "attachments"
            foreach (var file in attachments)
            {
                // Some browsers send file names with full path. We only care about the file name.
                var fileName = Path.GetFileName(file.FileName);
                var destinationPath = Path.Combine(Server.MapPath("~/App_Data"), fileName);

                file.SaveAs(destinationPath);
            }

            // Return an empty string to signify success
            return Content("");
        }

5. Build and run the application. The uploaded files will appear in the App_Data folder.

## Accessing an Existing Upload

You can reference an existing Upload instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/ui-widgets/upload/methods.aspx) to control its behavior.

### Accessing an existing Upload instance

    // Put this after your Kendo Upload for ASP.NET MVC declaration
    <script>
    $(function() {
        // Notice that the Name() of the Upload is used to get its client-side instance
        var upload = $("#attachments").data("kendoUpload");
    });
    </script>


## Handling Kendo UI Upload events

You can subscribe to all [events](http://www.kendoui.com/documentation/ui-widgets/upload/events.aspx) exposed by Kendo UI Upload:

### WebForms - subscribe by handler name

    <%: Html.Kendo().Upload()
            .Name("attachments")
            .Events(e => e
                .Upload("onUpload")
                .Success("onSuccess")
            )
    %>
    <script>
    function onUpload(e) {
        // Handle the upload event
    }

    function onSuccess() {
        // Handle the success event
    }
    </script>


### Razor - subscribe by handler name

    @(Html.Kendo().Upload()
            .Name("attachments")
            .Events(e => e
                .Upload("onUpload")
                .Success("onSuccess")
            )
    )
    <script>
    function onUpload(e) {
        // Handle the upload event
    }

    function onSuccess() {
        // Handle the success event
    }
    </script>


### Razor - subscribe by template delegate

    @(Html.Kendo().Upload()
          .Name("attachments")
          .Events(e => e
              .Upload(@<text>
                function() {
                    // Handle the upload event inline
                }
              </text>)
              .Success(@<text>
                function() {
                    // Handle the success event inline
                }
                </text>)
          )
    )
