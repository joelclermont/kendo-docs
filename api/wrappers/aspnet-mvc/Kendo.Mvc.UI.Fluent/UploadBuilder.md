---
title:UploadBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadBuilder

Defines the fluent interface for configuring the Upload component.

## Methods

### Events(System.Action\<Kendo.Mvc.UI.Fluent.UploadEventBuilder\>)
Configures the client-side events.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events
        .OnLoad("onLoad")
        .OnUpload("onUpload")
        )
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.UploadEventBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/UploadEventBuilder)\>
The client events configuration action.

### Enable(System.Boolean)
Enables or disables the component.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Enable(false)
        %>

#### Parameters

##### value `System.Boolean`
true if the component should be enabled, false otherwise; the default is true.

### Multiple(System.Boolean)
Enables or disables multiple file selection.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Multiple(false)
        %>

#### Parameters

##### value `System.Boolean`
true if multiple file selection should be enabled, false otherwise; the default is true.

### ShowFileList(System.Boolean)
Sets a value indicating whether to show the list of uploaded files

#### Parameters

##### value `System.Boolean`
true if the list of uploaded files should be visible, false otherwise; true by default

### Async(System.Action\<Kendo.Mvc.UI.Fluent.UploadAsyncSettingsBuilder\>)
Use it to configure asynchronous uploading.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Save", "Compose")
        .Remove("Remove", "Compose")
        );
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.UploadAsyncSettingsBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/UploadAsyncSettingsBuilder)\>
Use builder to set different asynchronous uploading options.

### Messages(System.Action\<Kendo.Mvc.UI.Fluent.UploadMessagesBuilder\>)
Use it to configure asynchronous uploading.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("Save", "Compose")
        .Remove("Remove", "Compose")
        );
        %>

#### Parameters

##### configurator System.Action\<[Kendo.Mvc.UI.Fluent.UploadMessagesBuilder](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/UploadMessagesBuilder)\>
Use builder to set different asynchronous uploading options.