---
title:SplitterBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.splitterbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SplitterBuilder

Defines the fluent interface for configuring the Splitter component.

## Methods

### Orientation(Kendo.Mvc.UI.SplitterOrientation)
Sets the splitter orientation.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Orientation(SplitterOrientation.Vertical)
        %>

#### Parameters

##### value [Kendo.Mvc.UI.SplitterOrientation](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI/SplitterOrientation)
The desired orientation.

### Panes(System.Action<Kendo.Mvc.UI.Fluent.SplitterPaneFactory>)
Defines the panes in the splitter.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add().LoadContentFrom("Navigation", "Shared");
        panes.Add().LoadContentFrom("Index", "Home");
        })
        %>

#### Parameters

##### configurePanes System.Action<[Kendo.Mvc.UI.Fluent.SplitterPaneFactory>](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/SplitterPaneFactory>)>
The action that configures the panes.

### Events(System.Action<Kendo.Mvc.UI.Fluent.SplitterEventBuilder>)
Configures the client events for the splitter.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Events(events => events
        .OnLoad("onLoad")
        )
        %>

#### Parameters

##### configureClientEvents System.Action<[Kendo.Mvc.UI.Fluent.SplitterEventBuilder>](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/SplitterEventBuilder>)>
The action that configures the client events.