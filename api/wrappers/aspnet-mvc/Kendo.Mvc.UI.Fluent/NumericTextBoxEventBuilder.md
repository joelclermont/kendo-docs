---
title:Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.numerictextboxeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder

## Methods

### Spin(System.String)
Defines the name of the JavaScript function that will handle the the Spin client-side event.

#### Example
    <%= Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events => events.Spin("spin"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.