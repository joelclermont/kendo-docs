---
title:Kendo.Mvc.UI.Fluent.TabStripBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.tabstripbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.TabStripBuilder

## Methods

### SecurityTrimming(System.Boolean)
Enable/disable security trimming functionality of the component.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .SecurityTrimming(false)
        %>

#### Parameters

##### value `System.Boolean`
If true security trimming is enabled.