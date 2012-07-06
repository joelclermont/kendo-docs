---
title:Kendo.Mvc.UI.Fluent.GaugeAreaBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugeareabuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeAreaBuilder

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the gauge area border.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .GaugeArea(gaugeArea => gaugeArea.Border(1, "#000", ChartDashType.Dot))
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The border width.

##### color `System.String`
The border color (CSS syntax).

##### dashType `Kendo.Mvc.UI.ChartDashType`
The border dash type.