---
title:Kendo.Mvc.UI.Fluent.DropDownListEventBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.dropdownlisteventbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.DropDownListEventBuilderBase

## Methods

### Close(System.String)
Defines the name of the JavaScript function that will handle the the Close client-side event.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Close("close"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.