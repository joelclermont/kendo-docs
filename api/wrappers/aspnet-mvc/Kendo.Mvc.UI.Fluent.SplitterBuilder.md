---
title:Kendo.Mvc.UI.Fluent.SplitterBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.splitterbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SplitterBuilder

## Methods

### Orientation(Kendo.Mvc.UI.SplitterOrientation)
Sets the splitter orientation.

#### Parameters

##### value `Kendo.Mvc.UI.SplitterOrientation`
The desired orientation.

#### Parameters

##### value `Kendo.Mvc.UI.SplitterOrientation`
The desired orientation.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Orientation(SplitterOrientation.Vertical)
        %>

### Panes(System.Action{Kendo.Mvc.UI.Fluent.SplitterPaneFactory})
Defines the panes in the splitter.

#### Parameters

##### configurePanes `System.Action{Kendo.Mvc.UI.Fluent.SplitterPaneFactory}`
The action that configures the panes.

#### Parameters

##### configurePanes `System.Action{Kendo.Mvc.UI.Fluent.SplitterPaneFactory}`
The action that configures the panes.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add().LoadContentFrom("Navigation", "Shared");
        panes.Add().LoadContentFrom("Index", "Home");
        })
        %>

### Events(System.Action{Kendo.Mvc.UI.Fluent.SplitterEventBuilder})
Configures the client events for the splitter.

#### Parameters

##### configureClientEvents `System.Action{Kendo.Mvc.UI.Fluent.SplitterEventBuilder}`
The action that configures the client events.

#### Parameters

##### configureClientEvents `System.Action{Kendo.Mvc.UI.Fluent.SplitterEventBuilder}`
The action that configures the client events.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events
        .OnLoad("onLoad")
        )
        %>