---
title:Kendo.Mvc.UI.Fluent.GaugeLabelsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.gaugelabelsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GaugeLabelsBuilder

## Methods

### Opacity(System.Double)
Sets the labels opacity.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        .Scale(scale => scale
        .Labels(labels => labels
        .Opacity(0.5)
        )
        )
        %>

#### Parameters

##### opacity `System.Double`

            The series opacity in the range from 0 (transparent) to 1 (opaque).
            The default value is 1.
            