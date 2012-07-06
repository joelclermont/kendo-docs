---
title:Kendo.Mvc.UI.Fluent.GridScrollSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridscrollsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridScrollSettingsBuilder

## Methods

### Height(System.String)
Sets the height of the scrollable.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Scrolling(scrolling => scrolling.Height("20em"))
        %>

#### Parameters

##### value `System.String`
The height in pixels.