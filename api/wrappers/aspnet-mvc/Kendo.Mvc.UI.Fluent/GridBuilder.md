---
title:Kendo.Mvc.UI.Fluent.GridBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gridbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridBuilder

## Methods

### Groupable
Allows grouping.

#### Example
    <%= Html.Kendo().Grid()
        .Name("Grid")
        .Ajax(ajax => ajax.Action("_RelatedGrids_Orders", "Grid", new { customerID = "ALFKI" }))
        .Columns(columns=>
        {
        columns.Add(c => c.OrderID).Width(100);
        columns.Add(c => c.OrderDate).Width(200).Format("{0:dd/MM/yyyy}");
        columns.Add(c => c.ShipAddress);
        columns.Add(c => c.ShipCity).Width(200);
        })
        .BindTo((IEnumerable<Order>)ViewData["Orders"])
        .Groupable();
        %>