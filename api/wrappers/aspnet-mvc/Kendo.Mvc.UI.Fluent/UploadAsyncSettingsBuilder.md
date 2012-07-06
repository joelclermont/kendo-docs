---
title:Kendo.Mvc.UI.Fluent.UploadAsyncSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadasyncsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadAsyncSettingsBuilder

## Methods

### RemoveField(System.String)
Sets the field name for the remove operation

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .RemoveField("attachments");
        )
        %>

#### Parameters

##### fieldName `System.String`

            The form field name to use for submiting the files.
            "fileNames" is used if not set.
            