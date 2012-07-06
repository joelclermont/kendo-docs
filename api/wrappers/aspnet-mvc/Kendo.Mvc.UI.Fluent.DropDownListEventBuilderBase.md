---
title:Kendo.Mvc.UI.Fluent.DropDownListEventBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.dropdownlisteventbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.DropDownListEventBuilderBase

## Methods

### Select(System.Func{System.Object,System.Object})
Defines the inline handler of the Select client-side event

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

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Select("select"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Change(System.Func{System.Object,System.Object})
Defines the inline handler of the Change client-side event

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

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

### Change(System.String)
Defines the name of the JavaScript function that will handle the the Change client-side event.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Change("onChange"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Open(System.String)
Defines the name of the JavaScript function that will handle the the Open client-side event.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Open("Open"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Open(System.Func{System.Object,System.Object})
Defines the inline handler of the Open client-side event

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

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

### Close(System.Func{System.Object,System.Object})
Defines the inline handler of the Close client-side event

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

#### Parameters

##### handler `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

### Close(System.String)
Defines the name of the JavaScript function that will handle the the Close client-side event.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Events(events => events.Close("close"))
        %>

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.