---
title:Kendo.Mvc.UI.Fluent.WindowActionsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.windowactionsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.WindowActionsBuilder

## Methods

### Clear
Configures the window to show no buttons in its titlebar.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Actions(actions => actions.Clear())
        %>