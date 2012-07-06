---
title:Kendo.Mvc.UI.Fluent.PageableBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.pageablebuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.PageableBuilder

## Methods

### Enabled(System.Boolean)
Enables or disables paging.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        .Pageable(paging => paging.Enabled((bool)ViewData["enablePaging"]))
        %>