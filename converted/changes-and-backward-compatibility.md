---
title: Changes and Backward Compatibility
publish: true
---

## KendoUI 2012 Q1 (2012.1.322)

### Changes from 2011 Q3 SP1 (2011.3.1407)

#### Breaking changes

The combined JavaScript file kendo.all.js is available only in the Kendo Complete package. The corresponding file in Kendo Web is called kendo.web.js. Use it instead of kendo.all.js.
 <style>
.content-main .prettyprint { overflow-x: auto; }
.content-main table { margin-top: 10px; }
</style> 

*   **Data: **kendo.model file has been removed. The content of kendo.model.js file has been consolidated with the kendo.data.js content.****
*   **Data: **Model.id is no longer a function. It is a field.
<table style="width: 100%;"> <colgroup> <col style="width: 50%;" /> <col style="width: 50%;" /> </colgroup> <tbody> <tr> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">Old</th> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">New</th> </tr> <tr> <td> 
    var model = dataSource.get(42);
    var modelId = model.id(); //42
                 </td> <td> 
    var model = dataSource.get(42);
    var modelId = model.id; //42
                 </td> </tr> </tbody> </table>*   **Data: **DataSource data contains **[ObservableObject](../../documentation/framework/MVVM/ObservableObject.aspx)s ** instead of **raw data records**.

*   **Grid:** The Grid widget is now using the `uid` field of the Model instead of the `id`. A new uid field is introduced to the DataSource's Model, which represents its unique id. The Grid row data attribute has been changed to use this field.
<table style="width: 100%;"> <colgroup> <col style="width: 50%;" /> <col style="width: 50%;" /> </colgroup> <tbody> <tr> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">Old</th> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">New</th> </tr> <tr> <td> 
    <tr data-id="42"><!--...--></tr>
                 </td> <td> 
    <tr data-uid=”aaaaa-bbbbb-ddddd-gggg”><!--...--></tr>
                 </td> </tr> </tbody> </table>
Note that in order to retrieve Model instance by its uid, DataSource's `getByUid` method should be used.

*   **DataViz: **The kendo.chart(.min).js file is replaced by kendo.dataviz(.min).js
*   **DataViz: **The axis orientation property deprecated in favor of dedicated verticalLine and verticalArea chart types
*   **DataViz**: The suite now requires kendo.dataviz.css to be included
*   **DataViz:** The Chart widget is now in the kendo.dataviz.ui namespace. Previously it was part of kendo.ui
*   **Other: **dataValueField and dataTextField of DropDownList, ComboBox and AutoComplete, are set to empty string by default. In order to get your old code working, you will need to list the fields manually, like this:
 <table width="693" height="78"> <tbody> <tr> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">Old</th> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">New</th> </tr> <tr> <td style="vertical-align: top;"> 
    $("#combobox").kendoComboBox([
    &nbsp;&nbsp;&nbsp; {text: "Item 1", value: "item1"},
    &nbsp;&nbsp;&nbsp; {text: "Item 2", value: "item2"}
    ]); </td> <td> 
    $("#combobox").kendoComboBox({
    &nbsp;&nbsp;&nbsp; dataTextField: "text",
    &nbsp;&nbsp;&nbsp; dataValueField: "value",
    &nbsp;&nbsp;&nbsp; dataSource: [
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; {text: "Item 1", value: "item1"},
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; {text: "Item 2", value: "item2"}
    &nbsp;&nbsp;&nbsp; ]
    }); </td> </tr> </tbody> </table> 

### Changes from 2011 Q3 Beta (2011.2.1007)

#### Breaking changes

*   Calendar: the `startView` property has been changed to `start`.
<table style="width: 100%;"> <colgroup> <col style="width: 50%;" /> <col style="width: 50%;" /> </colgroup> <tbody> <tr> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">Old</th> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">New</th> </tr> <tr> <td> 
    startView </td> <td> 
    start </td> </tr> <tr> <td> 
    $("#calendar").kendoCalendar({
    &nbsp;&nbsp;&nbsp; startView: "month"
    }) </td> <td> 
    $("#calendar").kendoCalendar({
    &nbsp;&nbsp;&nbsp; start: "month"
    }) </td> </tr> </tbody> </table>*   DatePicker: the `startView` property has been changed to `start`.
<table style="width: 100%;"> <colgroup> <col style="width: 50%;" /> <col style="width: 50%;" /> </colgroup> <tbody> <tr> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">Old</th> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">New</th> </tr> <tr> <td> 
    startView </td> <td> 
    start </td> </tr> <tr> <td> 
    $("#datepicker").kendoDatePicker({
    &nbsp;&nbsp;&nbsp; startView: "month"
    }) </td> <td> 
    $("#datepicker").kendoDatePicker({
    &nbsp;&nbsp;&nbsp; start: "month"
    }) </td> </tr> </tbody> </table>*   Window: the
`refresh(url, data)`
method has been changed to
`refresh(options)`
to allow overriding of request method, caching and other options. String arguments in the form of
`refresh(url)`
are still accepted.
<table style="width: 100%;"> <colgroup> <col style="width: 50%;" /> <col style="width: 50%;" /> </colgroup> <tbody> <tr> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">Old</th> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">New</th> </tr> <tr> <td> 
    refresh() </td> <td> 
    refresh() </td> </tr> <tr> <td> 
    refresh("/foo") </td> <td> 
    refresh("/foo") </td> </tr> <tr> <td style="vertical-align: top;"> 
    refresh("/foo", { bar: "baz" }) </td> <td style="vertical-align: top;"> 
    refresh({
    &nbsp;&nbsp;&nbsp; url: "/foo",
    &nbsp;&nbsp;&nbsp; data: { bar: "baz" }
    }) </td> </tr> </tbody> </table>*   Window: the `contentUrl` configuration option has been renamed to `content`. The content can be a URL or request options object.
<table style="width: 100%;"> <colgroup> <col style="width: 50%;" /> <col style="width: 50%;" /> </colgroup> <tbody> <tr> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">Old</th> <th align="left" style="border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: #999999;">New</th> </tr> <tr> <td style="vertical-align: top;"> 
    $("<div />").kendoWindow({
        // ...
        contentUrl: "/foo"
    }); </td> <td style="vertical-align: top;"> 
    $("<div />").kendoWindow({
        // ...
        content: "/foo"
    }); </td> </tr> </tbody> </table>