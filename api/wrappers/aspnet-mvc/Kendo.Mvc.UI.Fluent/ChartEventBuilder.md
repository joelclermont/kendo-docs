---
title:ChartEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.charteventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartEventBuilder

Defines the fluent interface for configuring the ChartClientEvents.

## Methods

### DataBound(System.Func<System.Object,System.Object>)
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

##### inlineCodeBlock `System.Func<System.Object`
The handler code wrapped in a text tag (Razor syntax).

### DataBound(System.String)
Defines the name of the JavaScript function that will handle the the DataBound client-side event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.DataBound("onDataBound"))
        %>

#### Parameters

##### onDataBoundHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### DataBinding(System.Func<System.Object,System.Object>)
Defines the inline handler of the DataBinding client-side event

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

#### Parameters

##### inlineCodeBlock `System.Func<System.Object`
The handler code wrapped in a text tag (Razor syntax).

### DataBinding(System.String)
Defines the name of the JavaScript function that will handle the the DataBinding client-side event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.DataBinding("onDataBinding"))
        %>

#### Parameters

##### onDataBindingHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### SeriesClick(System.Func<System.Object,System.Object>)
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

##### inlineCodeBlock `System.Func<System.Object`
The handler code wrapped in a text tag (Razor syntax).

### SeriesClick(System.String)
Defines the name of the JavaScript function that will handle the the SeriesClick client-side event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.SeriesClick("onSeriesClick"))
        %>

#### Parameters

##### onSeriesClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### SeriesHover(System.Func<System.Object,System.Object>)
Defines the inline handler of the SeriesHover client-side event

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

#### Parameters

##### inlineCodeBlock `System.Func<System.Object`
The handler code wrapped in a text tag (Razor syntax).

### SeriesHover(System.String)
Defines the name of the JavaScript function that will handle the the SeriesHover client-side event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.SeriesHover("onSeriesHover"))
        %>

#### Parameters

##### onSeriesHoverHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### AxisLabelClick(System.Func<System.Object,System.Object>)
Defines the inline handler of the AxisLabelClick client-side event

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

#### Parameters

##### inlineCodeBlock `System.Func<System.Object`
The handler code wrapped in a text tag (Razor syntax).

### AxisLabelClick(System.String)
Defines the name of the JavaScript function that will handle the the AxisLabelClick client-side event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.AxisLabelClick("onAxisLabelClick"))
        %>

#### Parameters

##### onAxisLabelClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### PlotAreaClick(System.Func<System.Object,System.Object>)
Defines the inline handler of the PlotAreaClick client-side event

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

#### Parameters

##### inlineCodeBlock `System.Func<System.Object`
The handler code wrapped in a text tag (Razor syntax).

### PlotAreaClick(System.String)
Defines the name of the JavaScript function that will handle the the PlotAreaClick client-side event.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events.PlotAreaClick("onPlotAreaClick"))
        %>

#### Parameters

##### onPlotAreaClickHandlerName `System.String`
The name of the JavaScript function that will handle the event.