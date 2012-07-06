---
title:Kendo.Mvc.UI.Fluent.SplitterEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.splittereventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SplitterEventBuilder

## Methods

### ContentLoad(System.String)
Defines the name of the JavaScript function that will handle the the ContentLoad client-side event.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events.ContentLoad("onContentLoad"))
        %>

#### Parameters

##### onContentLoadHandlerName `System.String`
The name of the JavaScript function that will handle the event.