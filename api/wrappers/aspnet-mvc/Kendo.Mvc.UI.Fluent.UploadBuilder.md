---
title:Kendo.Mvc.UI.Fluent.UploadBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadBuilder

## Methods

### Events(System.Action{Kendo.Mvc.UI.Fluent.UploadEventBuilder})
Configures the client-side events.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.UploadEventBuilder}`
The client events configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.UploadEventBuilder}`
The client events configuration action.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events
        .OnLoad("onLoad")
        .OnUpload("onUpload")
        )
        %>

### Enable(System.Boolean)
Enables or disables the component.

#### Parameters

##### value `System.Boolean`
true if the component should be enabled, false otherwise; the default is true.

#### Parameters

##### value `System.Boolean`
true if the component should be enabled, false otherwise; the default is true.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Enable(false)
        %>

### Multiple(System.Boolean)
Enables or disables multiple file selection.

#### Parameters

##### value `System.Boolean`
true if multiple file selection should be enabled, false otherwise; the default is true.

#### Parameters

##### value `System.Boolean`
true if multiple file selection should be enabled, false otherwise; the default is true.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Multiple(false)
        %>

### ShowFileList(System.Boolean)
Sets a value indicating whether to show the list of uploaded files

#### Parameters

##### value `System.Boolean`
true if the list of uploaded files should be visible, false otherwise; true by default

#### Parameters

##### value `System.Boolean`
true if the list of uploaded files should be visible, false otherwise; true by default

### Async(System.Action{Kendo.Mvc.UI.Fluent.UploadAsyncSettingsBuilder})
Use it to configure asynchronous uploading.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.UploadAsyncSettingsBuilder}`
Use builder to set different asynchronous uploading options.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.UploadAsyncSettingsBuilder}`
Use builder to set different asynchronous uploading options.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Save", "Compose")
        .Remove("Remove", "Compose")
        );
        %>

### Messages(System.Action{Kendo.Mvc.UI.Fluent.UploadMessagesBuilder})
Use it to configure asynchronous uploading.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.UploadMessagesBuilder}`
Use builder to set different asynchronous uploading options.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.UploadMessagesBuilder}`
Use builder to set different asynchronous uploading options.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Save", "Compose")
        .Remove("Remove", "Compose")
        );
        %>