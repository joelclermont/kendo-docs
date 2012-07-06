---
title:Kendo.Mvc.UI.Fluent.ChartEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charteventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartEventBuilder

## Methods

### SeriesClick(System.Func{System.Object,System.Object})
Defines the inline handler of the SeriesClick client-side event

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.SeriesClick(
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