---
title:Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartnumericaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder

## Methods

### Max(System.Double)
Sets the axis maximum value.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric().Max(4))
        %>

#### Parameters

##### max `System.Double`
The axis maximum value.