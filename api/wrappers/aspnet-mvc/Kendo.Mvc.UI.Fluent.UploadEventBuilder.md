---
title:Kendo.Mvc.UI.Fluent.UploadEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.uploadeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.UploadEventBuilder

## Methods

### Select(System.Func{System.Object,System.Object})
Defines the inline handler of the Select client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Select(System.String)
Defines the name of the JavaScript function that will handle the the Select client-side event.

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onSelectHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Select("onSelect"))
        %>

### Upload(System.Func{System.Object,System.Object})
Defines the inline handler of the Upload client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Upload(System.String)
Defines the name of the JavaScript function that will handle the the Upload client-side event.

#### Parameters

##### onUploadHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onUploadHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Upload("onUpload"))
        %>

### Success(System.Func{System.Object,System.Object})
Defines the inline handler of the Success client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Success(System.String)
Defines the name of the JavaScript function that will handle the the Success client-side event.

#### Parameters

##### onSuccessHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onSuccessHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Success("onSuccess"))
        %>

### Error(System.Func{System.Object,System.Object})
Defines the inline handler of the Error client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Parameters

##### onErrorHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onErrorHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Error("onError"))
        %>

### Complete(System.Func{System.Object,System.Object})
Defines the inline handler of the Complete client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Complete(System.String)
Defines the name of the JavaScript function that will handle the the Complete client-side event.

#### Parameters

##### onCompleteHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onCompleteHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Complete("onComplete"))
        %>

### Cancel(System.Func{System.Object,System.Object})
Defines the inline handler of the Cancel client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Cancel(System.String)
Defines the name of the JavaScript function that will handle the the Cancel client-side event.

#### Parameters

##### onCancelHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onCancelHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Cancel("onCancel"))
        %>

### Remove(System.Func{System.Object,System.Object})
Defines the inline handler of the Remove client-side event

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

#### Parameters

##### inlineCodeBlock `System.Func{System.Object`
The handler code wrapped in a text tag (Razor syntax).

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

### Remove(System.String)
Defines the name of the JavaScript function that will handle the the Remove client-side event.

#### Parameters

##### onRemoveHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Parameters

##### onRemoveHandlerName `System.String`
The name of the JavaScript function that will handle the event.

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Events(events => events.Remove("onRemove"))
        %>