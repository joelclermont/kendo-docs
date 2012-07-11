---
title:GridEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.grideventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.GridEventBuilder

Defines the fluent API for configuring the Kendo Grid for ASP.NET MVC events.

## Methods

### Change(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Change client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.Change(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Change(System.String)
Defines the name of the JavaScript function that will handle the the Change client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.Change("gridChange"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Edit(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Edit client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.Edit(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Edit(System.String)
Defines the name of the JavaScript function that will handle the the Edit client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.Edit("gridEdit"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Save(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Save client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.Save(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Save(System.String)
Defines the name of the JavaScript function that will handle the the Save client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.Save("gridSave"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### SaveChanges(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the SaveChanges client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.SaveChanges(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### SaveChanges(System.String)
Defines the name of the JavaScript function that will handle the the SaveChanges client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.SaveChanges("gridSaveChanges"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### DetailExpand(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the DetailExpand client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.DetailExpand(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### DetailExpand(System.String)
Defines the name of the JavaScript function that will handle the the DetailExpand client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.DetailExpand("gridDetailExpand"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### DetailInit(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the DetailInit client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.DetailInit(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### DetailInit(System.String)
Defines the name of the JavaScript function that will handle the the DetailInit client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.DetailInit("gridDetailInit"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### DetailCollapse(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the DetailCollapse client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.DetailCollapse(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### DetailCollapse(System.String)
Defines the name of the JavaScript function that will handle the the DetailCollapse client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.DetailCollapse("gridDetailCollapse"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Remove(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the Remove client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.Remove(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Remove(System.String)
Defines the name of the JavaScript function that will handle the the Remove client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.Remove("gridRemove"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### DataBound(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the DataBound client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.DataBound(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### DataBound(System.String)
Defines the name of the JavaScript function that will handle the the DataBound client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.DataBound("gridDataBound"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### ColumnResize(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the ColumnResize client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.ColumnResize(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### ColumnResize(System.String)
Defines the name of the JavaScript function that will handle the the ColumnResize client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.ColumnResize("gridColumnResize"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### ColumnReorder(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the ColumnReorder client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.ColumnReorder(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### ColumnReorder(System.String)
Defines the name of the JavaScript function that will handle the the ColumnReorder client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.ColumnReorder("gridColumnReorder"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### ColumnHide(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the ColumnHide client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.ColumnHide(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### ColumnHide(System.String)
Defines the name of the JavaScript function that will handle the the ColumnHide client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.ColumnHide("gridColumnHide"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### ColumnShow(System.Func\<System.Object,System.Object\>)
Defines the name of the JavaScript function that will handle the the ColumnShow client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.ColumnShow(
        @<text>
        function(e) {
        //event handling code
        }
        </text>
        ))
        )

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### ColumnShow(System.String)
Defines the name of the JavaScript function that will handle the the ColumnShow client-side event.

#### Example
    @(Html.Kendo().Grid()
        .Name("Grid")
        .Events(events => events.ColumnShow("gridColumnShow"))
        )

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.