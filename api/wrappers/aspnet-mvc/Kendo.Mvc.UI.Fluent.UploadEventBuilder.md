---
title:Kendo.Mvc.UI.Fluent.UploadEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadEventBuilder

## Methods

### Select(System.Func{System.Object,System.Object})
Defines the inline handler of the Select client-side event

#### Example
    <% Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Select(
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

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Select("onSelect"))
        %>

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Upload(System.Func{System.Object,System.Object})
Defines the inline handler of the Upload client-side event

#### Example
    <% Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Upload(
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

### Upload(System.String)
Defines the name of the JavaScript function that will handle the the Upload client-side event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Upload("onUpload"))
        %>

#### Parameters

##### onUploadHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Success(System.Func{System.Object,System.Object})
Defines the inline handler of the Success client-side event

#### Example
    <% Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Success(
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

### Success(System.String)
Defines the name of the JavaScript function that will handle the the Success client-side event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Success("onSuccess"))
        %>

#### Parameters

##### onSuccessHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Error(System.Func{System.Object,System.Object})
Defines the inline handler of the Error client-side event

#### Example
    <% Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Error(
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

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Error("onError"))
        %>

#### Parameters

##### onErrorHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Complete(System.Func{System.Object,System.Object})
Defines the inline handler of the Complete client-side event

#### Example
    <% Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Complete(
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

### Complete(System.String)
Defines the name of the JavaScript function that will handle the the Complete client-side event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Complete("onComplete"))
        %>

#### Parameters

##### onCompleteHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Cancel(System.Func{System.Object,System.Object})
Defines the inline handler of the Cancel client-side event

#### Example
    <% Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Cancel(
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

### Cancel(System.String)
Defines the name of the JavaScript function that will handle the the Cancel client-side event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Cancel("onCancel"))
        %>

#### Parameters

##### onCancelHandlerName `System.String`
The name of the JavaScript function that will handle the event.

### Remove(System.Func{System.Object,System.Object})
Defines the inline handler of the Remove client-side event

#### Example
    <% Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Remove(
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

### Remove(System.String)
Defines the name of the JavaScript function that will handle the the Remove client-side event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Remove("onRemove"))
        %>

#### Parameters

##### onRemoveHandlerName `System.String`
The name of the JavaScript function that will handle the event.