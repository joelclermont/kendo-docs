---
title:Kendo.Mvc.UI.Fluent.MenuBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.menubuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.MenuBuilder

## Methods

### SecurityTrimming(System.Boolean)
Enable/disable security trimming functionality of the component.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .SecurityTrimming(false)
        %>

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.