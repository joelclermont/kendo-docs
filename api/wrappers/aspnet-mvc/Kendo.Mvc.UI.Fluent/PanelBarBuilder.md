---
title:Kendo.Mvc.UI.Fluent.PanelBarBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.panelbarbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PanelBarBuilder

## Methods

### SecurityTrimming(System.Boolean)
Enable/disable security trimming functionality of the component.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .SecurityTrimming(false)
        %>

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.