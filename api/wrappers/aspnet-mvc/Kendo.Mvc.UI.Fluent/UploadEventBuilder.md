---
title:Kendo.Mvc.UI.Fluent.UploadEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadEventBuilder

## Methods

### Remove(System.String)
Defines the name of the JavaScript function that will handle the the Remove client-side event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Remove("onRemove"))
        %>

#### Parameters

##### onRemoveHandlerName `System.String`
The name of the JavaScript function that will handle the event.