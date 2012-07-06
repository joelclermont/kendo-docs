---
title:Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartnumericaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder

## Methods

### Min(System.Double)
Sets the axis minimum value.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric().Min(4))
        %>

#### Parameters

##### min `System.Double`
The axis minimum value.