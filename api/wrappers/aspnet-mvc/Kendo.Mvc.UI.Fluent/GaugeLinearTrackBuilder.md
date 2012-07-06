---
title:Kendo.Mvc.UI.Fluent.GaugeLinearTrackBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelineartrackbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLinearTrackBuilder

## Methods

### Border(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets the track border.

#### Example
    <% Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Pointer(pointer => pointer
        .Track(track => track.Border(1, "#000", ChartDashType.Dot))
        )
        .Render();
        %>

#### Parameters

##### width `System.Int32`
The pointer border width.

##### color `System.String`
The pointer border color.

##### dashType `Kendo.Mvc.UI.ChartDashType`
The pointer dash type.