---
title:Kendo.Mvc.UI.Fluent.UploadBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadBuilder

## Methods

### Messages(System.Action{Kendo.Mvc.UI.Fluent.UploadMessagesBuilder})
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

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.UploadMessagesBuilder}`
Use builder to set different asynchronous uploading options.