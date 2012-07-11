---
title:DataSourceEventBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.datasourceeventbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.DataSourceEventBuilder

Defines the fluent interface for configuring the DataSource component client-side events.

## Methods

### Change(System.String)
Defines the name of the JavaScript function that will handle the the Change client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Change(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Change client-side event.

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### RequestStart(System.String)
Defines the name of the JavaScript function that will handle the the RequestStart client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### RequestStart(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the RequestStart client-side event.

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).

### Error(System.String)
Defines the name of the JavaScript function that will handle the the Error client-side event.

#### Parameters

##### handler `System.String`
The name of the JavaScript function that will handle the event.

### Error(System.Func\<System.Object,System.Object\>)
Defines the inline handler of the Error client-side event.

#### Parameters

##### handler `System.Func<System.Object,System.Object>`
The handler code wrapped in a text tag (Razor syntax).