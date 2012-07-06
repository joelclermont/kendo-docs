---
title:Kendo.Mvc.UI.Fluent.UploadMessagesBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadmessagesbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadMessagesBuilder

## Methods

### Cancel(System.String)
Sets the Cancel button text

#### Parameters

##### cancelMessage `System.String`
New cancel button text.

#### Parameters

##### cancelMessage `System.String`
New cancel button text.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .Cancel("cancel")
        )
        %>

### Remove(System.String)
Sets the Remove button text

#### Parameters

##### removeMessage `System.String`
New Remove button text.

#### Parameters

##### removeMessage `System.String`
New Remove button text.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .Remove("drop files here")
        )
        %>

### Retry(System.String)
Sets the Retry button text

#### Parameters

##### retryMessage `System.String`
New Retry button text.

#### Parameters

##### retryMessage `System.String`
New Retry button text.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .Retry("retry")
        )
        %>

### Select(System.String)
Sets the Select button text

#### Parameters

##### selectMessage `System.String`
New Select button text.

#### Parameters

##### selectMessage `System.String`
New Select button text.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .Select("select")
        )
        %>

### StatusFailed(System.String)
Sets the "failed" status text accessible by screen readers

#### Parameters

##### statusFailedMessage `System.String`
New "failed" status text accessible by screen readers.

#### Parameters

##### statusFailedMessage `System.String`
New "failed" status text accessible by screen readers.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .StatusFailed("failed")
        )
        %>

### StatusUploaded(System.String)
Sets the "uploaded" status text accessible by screen readers

#### Parameters

##### statusUploadedMessage `System.String`
New "uploaded" status text accessible by screen readers.

#### Parameters

##### statusUploadedMessage `System.String`
New "uploaded" status text accessible by screen readers.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .StatusUploaded("uploaded")
        )
        %>

### StatusUploading(System.String)
Sets the "uploading" status text accessible by screen readers

#### Parameters

##### statusUploadingMessage `System.String`
New "uploading" status text accessible by screen readers.

#### Parameters

##### statusUploadingMessage `System.String`
New "uploading" status text accessible by screen readers.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .StatusUploading("uploading")
        )
        %>

### UploadSelectedFiles(System.String)
Sets Upload button (visible when AutoUpload is set to false) text

#### Parameters

##### uploadSelectedFilesMessage `System.String`
New Upload button text.

#### Parameters

##### uploadSelectedFilesMessage `System.String`
New Upload button text.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Messages(msgs => msgs
        .UploadSelectedFiles("uploading")
        )
        %>