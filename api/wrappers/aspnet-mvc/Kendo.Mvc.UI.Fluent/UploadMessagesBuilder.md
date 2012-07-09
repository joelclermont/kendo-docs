---
title:Kendo.Mvc.UI.Fluent.UploadMessagesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadmessagesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadMessagesBuilder

A builder class for UploadMessages

## Methods

### Cancel(System.String)
Sets the Cancel button text

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .Cancel("cancel")
        )
        %>

#### Parameters

##### cancelMessage `System.String`
New cancel button text.

### Remove(System.String)
Sets the Remove button text

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .Remove("drop files here")
        )
        %>

#### Parameters

##### removeMessage `System.String`
New Remove button text.

### Retry(System.String)
Sets the Retry button text

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .Retry("retry")
        )
        %>

#### Parameters

##### retryMessage `System.String`
New Retry button text.

### Select(System.String)
Sets the Select button text

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .Select("select")
        )
        %>

#### Parameters

##### selectMessage `System.String`
New Select button text.

### StatusFailed(System.String)
Sets the "failed" status text accessible by screen readers

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .StatusFailed("failed")
        )
        %>

#### Parameters

##### statusFailedMessage `System.String`
New "failed" status text accessible by screen readers.

### StatusUploaded(System.String)
Sets the "uploaded" status text accessible by screen readers

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .StatusUploaded("uploaded")
        )
        %>

#### Parameters

##### statusUploadedMessage `System.String`
New "uploaded" status text accessible by screen readers.

### StatusUploading(System.String)
Sets the "uploading" status text accessible by screen readers

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .StatusUploading("uploading")
        )
        %>

#### Parameters

##### statusUploadingMessage `System.String`
New "uploading" status text accessible by screen readers.

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