---
title:Kendo.Mvc.UI.Fluent.UploadMessagesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadmessagesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadMessagesBuilder

## Methods

### UploadSelectedFiles(System.String)
Sets Upload button (visible when AutoUpload is set to false) text

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .UploadSelectedFiles("uploading")
        )
        %>

#### Parameters

##### uploadSelectedFilesMessage `System.String`
New Upload button text.