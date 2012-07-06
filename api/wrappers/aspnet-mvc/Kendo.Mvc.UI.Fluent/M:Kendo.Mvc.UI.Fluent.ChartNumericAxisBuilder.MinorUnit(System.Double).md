---
title:Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartnumericaxisbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartNumericAxisBuilder

## Methods

### MinorUnit(System.Double)
Sets the interval between minor divisions.
            It defaults to MajorUnit / 5.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric()
        .MajorUnit(4)
        .MinorUnit(2)
        .MinorTicks(mt => mt.Visible(true))
        )
        %>

#### Parameters

##### minorUnit `System.Double`
The interval between minor divisions.