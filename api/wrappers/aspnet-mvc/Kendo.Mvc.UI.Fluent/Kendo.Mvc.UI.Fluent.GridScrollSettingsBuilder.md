---
title:Kendo.Mvc.UI.Fluent.GridScrollSettingsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridscrollsettingsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridScrollSettingsBuilder

## Methods

### Enabled(System.Boolean)
Enables or disables scrolling.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Scrolling(scrolling => scrolling.Enabled((bool)ViewData["enableScrolling"]))
        %>

### Height(System.Int32)
Sets the height of the scrollable area in pixels.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Scrolling(scrolling => scrolling.Height(400))
        %>

#### Parameters

##### pixelHeight `System.Int32`
The height in pixels.

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