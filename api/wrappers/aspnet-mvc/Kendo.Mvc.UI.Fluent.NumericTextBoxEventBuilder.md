---
title:Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.numerictextboxeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder

## Methods

### Change(System.Func{System.Object,System.Object})
Defines the inline handler of the Change client-side event

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events => events.Change(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### Change(System.String)
Defines the name of the JavaScript function that will handle the the Change client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events => events.Change("change"))
        %>

### Spin(System.Func{System.Object,System.Object})
Defines the inline handler of the Spin client-side event

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events => events.Spin(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### Spin(System.String)
Defines the name of the JavaScript function that will handle the the Spin client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events => events.Spin("spin"))
        %>