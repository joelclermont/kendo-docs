---
title:Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartnumericaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder

## Methods

### MajorUnit(System.Double)
Sets the interval between major divisions.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric().MajorUnit(4))
        %>

#### Parameters

##### majorUnit `System.Double`
The interval between major divisions.