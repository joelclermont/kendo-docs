---
title:Kendo.Mvc.UI.Fluent.ChartEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charteventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartEventBuilder

## Methods

### DataBound(System.Func{System.Object,System.Object})
Defines the inline handler of the DataBound client-side event

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.DataBound(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).