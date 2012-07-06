---
title:Kendo.Mvc.UI.Fluent.ListViewBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.listviewbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ListViewBuilder

## Methods

### Events(System.Action{Kendo.Mvc.UI.Fluent.ListViewEventBuilder})
Configures the client-side events.

#### Example
    <%= Html.Kendo().ListView()
        .Name("ListView")
        .Events(events => events
        .DataBound("onDataBound")
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ListViewEventBuilder}`
The client events action.