---
title:Kendo.Mvc.UI.Fluent.SplitterPaneBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.splitterpanebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.SplitterPaneBuilder

## Methods

### LoadContentFrom(System.String)
Sets the Url, which will be requested to return the pane content.

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter")
        .Panes(panes => {
        panes.Add()
        .LoadContentFrom(Url.Action("AjaxView_OpenSource", "Splitter"));
        })
        %>

#### Parameters

##### value `System.String`
The url.