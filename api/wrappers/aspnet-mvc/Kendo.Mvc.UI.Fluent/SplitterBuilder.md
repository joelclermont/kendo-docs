---
title:Kendo.Mvc.UI.Fluent.SplitterBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.splitterbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SplitterBuilder

## Methods

### Events(System.Action{Kendo.Mvc.UI.Fluent.SplitterEventBuilder})
Configures the client events for the splitter.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events
        .OnLoad("onLoad")
        )
        %>

#### Parameters

##### configureClientEvents `System.Action{Kendo.Mvc.UI.Fluent.SplitterEventBuilder}`
The action that configures the client events.