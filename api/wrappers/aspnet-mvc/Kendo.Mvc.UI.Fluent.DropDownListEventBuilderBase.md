---
title:Kendo.Mvc.UI.Fluent.DropDownListEventBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.dropdownlisteventbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.DropDownListEventBuilderBase

## Methods

### Select(System.Func{System.Object,System.Object})
Defines the inline handler of the Select client-side event

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Select(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        %>

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Select("select"))
        %>

### Change(System.Func{System.Object,System.Object})
Defines the inline handler of the Change client-side event

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Change(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
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
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Change("onChange"))
        %>

### Open(System.String)
Defines the name of the JavaScript function that will handle the the Open client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Open("Open"))
        %>

### Open(System.Func{System.Object,System.Object})
Defines the inline handler of the Open client-side event

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Open(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        %>

### Close(System.Func{System.Object,System.Object})
Defines the inline handler of the Close client-side event

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Close(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        %>

### Close(System.String)
Defines the name of the JavaScript function that will handle the the Close client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Close("close"))
        %>