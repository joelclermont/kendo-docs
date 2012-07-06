---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### Events(System.Action{Kendo.Mvc.UI.Fluent.ChartEventBuilder})
Configures the client-side events.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events
        .OnLoad("onLoad")
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartEventBuilder}`
The client events configuration action.