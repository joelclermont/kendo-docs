---
title:Kendo.Mvc.UI.Fluent.ChartEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charteventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartEventBuilder

## Methods

### DataBound(System.Func{System.Object,System.Object})
Defines the inline handler of the DataBound client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### DataBound(System.String)
Defines the name of the JavaScript function that will handle the the DataBound client-side event.

#### Parameters

##### onDataBoundHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onDataBoundHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.DataBound("onDataBound"))
        %>

### DataBinding(System.Func{System.Object,System.Object})
Defines the inline handler of the DataBinding client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.DataBinding(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### DataBinding(System.String)
Defines the name of the JavaScript function that will handle the the DataBinding client-side event.

#### Parameters

##### onDataBindingHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onDataBindingHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.DataBinding("onDataBinding"))
        %>

### SeriesClick(System.Func{System.Object,System.Object})
Defines the inline handler of the SeriesClick client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### SeriesClick(System.String)
Defines the name of the JavaScript function that will handle the the SeriesClick client-side event.

#### Parameters

##### onSeriesClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onSeriesClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.SeriesClick("onSeriesClick"))
        %>

### SeriesHover(System.Func{System.Object,System.Object})
Defines the inline handler of the SeriesHover client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.SeriesHover(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### SeriesHover(System.String)
Defines the name of the JavaScript function that will handle the the SeriesHover client-side event.

#### Parameters

##### onSeriesHoverHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onSeriesHoverHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.SeriesHover("onSeriesHover"))
        %>

### AxisLabelClick(System.Func{System.Object,System.Object})
Defines the inline handler of the AxisLabelClick client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.AxisLabelClick(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### AxisLabelClick(System.String)
Defines the name of the JavaScript function that will handle the the AxisLabelClick client-side event.

#### Parameters

##### onAxisLabelClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onAxisLabelClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.AxisLabelClick("onAxisLabelClick"))
        %>

### PlotAreaClick(System.Func{System.Object,System.Object})
Defines the inline handler of the PlotAreaClick client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Example
    <% Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.PlotAreaClick(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        .Render();
        %>

### PlotAreaClick(System.String)
Defines the name of the JavaScript function that will handle the the PlotAreaClick client-side event.

#### Parameters

##### onPlotAreaClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onPlotAreaClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.PlotAreaClick("onPlotAreaClick"))
        %>