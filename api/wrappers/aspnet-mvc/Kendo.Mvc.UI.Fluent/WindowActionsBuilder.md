---
title:Kendo.Mvc.UI.Fluent.WindowActionsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.windowactionsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.WindowActionsBuilder

Defines the fluent interface for configuring the Actions.

## Methods

### Close
Configures the window to show a close button.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Actions(actions => actions.Close())
        %>

### Maximize
Configures the window to show a maximize button.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Actions(actions => actions.Maximize())
        %>

### Minimize
Configures the window to show a minimize button.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Actions(actions => actions.Maximize())
        %>

### Refresh
Configures the window to show a refresh button.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Actions(actions => actions.Refresh())
        %>

### Custom(System.String)
Configures the window to show a refresh button.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Actions(actions => actions.Custom("menu"))
        %>

### Clear
Configures the window to show no buttons in its titlebar.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Actions(actions => actions.Clear())
        %>