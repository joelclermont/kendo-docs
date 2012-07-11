---
title: Javascript Dependencies
slug: gs-javascript-dependencies
publish: true
---

# JavaScript files used by Kendo UI

Every widget from **Kendo UI** needs its JavaScript files to be included in order to work properly. This help topic lists the JavaScript files required by each widget.

## Combined Scripts

The following combined scripts are made available in order to simplify development and deployment.

*   **kendo.all.min.js** contains a minified version of all scripts (Web, DataViz and Mobile).

> kendo.all.min.js is only available in the Kendo UI Complete package.

*   **kendo.web.min.js** contains a minified version of all scripts from Kendo UI Web.
*   **kendo.dataviz.min.js** contains a minified version of all scripts from Kendo UI DataViz.
*   **kendo.mobile.min.js** contains a minified version of all scripts from Kendo UI Mobile.

**Important:** Only one of the above scripts can be included at a time.

## Custom Combined Scripts

Users who own a commercial license can use the [custom download builder tool](http://www.kendoui.com/custom-download)
to create a single JavaScript file which contains only the required widgets and features.

## CDN

The minified versions of all JavaScript files (except jQuery) are also available via CDN

    http://cdn.kendostatic.com/<version>/js/<filename>.min.js

**e.g.** `http://cdn.kendostatic.com/2012.2.710/js/kendo.all.min.js`

> **Important:** in order to use HTTPS, you need to directly access the CloudFront CDN

    https://da7xgjtj801h2.cloudfront.net/<version>/js/<filename>.min.js

## Individual scripts

If more granular control is required, the following script files, either minified or not,
can be included on a per-widget basis.

### AutoComplete

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js
7.  kendo.fx.js (optional for animation)
8.  kendo.popup.js
9.  kendo.list.js
10.  kendo.autocomplete.js


### Calendar

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (optional for animation)
4.  kendo.calendar.js

### Chart

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.data.xml.js (if binding to XML)
5.  kendo.data.js
6.  <span>kendo.binder.js (if using MVVM)</span>
7.  kendo.dataviz.core.js
8.  kendo.dataviz.vml.js
9.  kendo.dataviz.svg.js
10.  kendo.dataviz.chart.js


### ComboBox

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js
7.  kendo.fx.js (optional for animation)
8.  kendo.popup.js
9.  kendo.list.js
10.  kendo.combobox.js


### DataSource

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML or editing)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js


### DatePicker

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (optional for animation)
4.  kendo.popup.js
5.  kendo.calendar.js
6.  kendo.datepicker.js


### Drag and Drop

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.draganddrop.js


### DropDownList

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js
7.  kendo.fx.js (optional for animation)
8.  kendo.popup.js
9.  kendo.list.js
10.  kendo.dropdownlist.js


### Editor

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.popup.js
4.  kendo.list.js
5.  kendo.dropdownlist.js
6.  kendo.combobox.js
7.  kendo.fx.js (optional for animation)
8.  kendo.draganddrop.js (if popups are draggable and/or resizable)
9.  kendo.window.js
10.  kendo.editor.js


### Gauge

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.js (if using MVVM)
4.  kendo.binder.js (if using MVVM)
5.  kendo.dataviz.core.js
6.  kendo.dataviz.vml.js
7.  kendo.dataviz.svg.js
8.  kendo.dataviz.gauge.js


### Grid

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.data.xml.js (if binding to XML)
5.  kendo.data.js
6.  kendo.fx.js (optional for animation)
6.  kendo.popup.js (if editing or filtering is enabled)
7.  kendo.list.js&nbsp;(if editing or filtering is enabled)
8.  kendo.calendar.js (if editing or filtering is enabled)
9.  kendo.datepicker.js (if editing or filtering is enabled)
10.  kendo.numerictextbox.js (if editing or filtering is enabled)
11.  kendo.validator.js (if editing is enabled)
12.  kendo.binder.js (if editing is enabled)
13.  kendo.dropdownlist.js (if filtering is enabled)
14.  kendo.filtermenu.js (if filtering is enabled)
15.  kendo.pager.js (if paging is enabled)
16.  kendo.sortable.js (if sorting is enabled)
17.  kendo.draganddrop.js (if grouping, resizing or reordering is enabled)
18.  kendo.groupable.js (if grouping is enabled)
19.  kendo.editable.js (if editing is enabled)
20.  kendo.selectable.js (if selection is enabled)
21.  kendo.resizable.js (if resizing is enabled)
22.  kendo.reorderable.js (if reordering is enabled)
23.  kendo.grid.js


### ListView

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.data.xml.js (if binding to XML)
5.  kendo.data.js
6.  kendo.validator.js (if editing is enabled)
7.  kendo.binder.js (if editing is enabled)
8.  kendo.pager.js (if pager is used)
9.  kendo.editable.js (if editing is enabled)
10.  kendo.selectable.js (if selection is enabled)
11.  kendo.listview.js


### Menu

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (optional for animation)
4.  kendo.popup.js
5.  kendo.menu.js


### NumericTextBox

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.numerictextbox.js


### PanelBar

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (optional for animation)
4.  kendo.panelbar.js


### Slider and RangeSlider

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.binder.js (if using MVVM)
4.  kendo.draganddrop.js
5.  kendo.slider.js


### Splitter

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.draganddrop.js
4.  kendo.resizable.js
5.  kendo.splitter.js


### TabStrip

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.js
3.  kendo.fx.js (optional for animation)
5.  kendo.tabstrip.js


### TimePicker

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (optional for animation)
4.  kendo.popup.js
5.  kendo.timepicker.js


### TreeView

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.js
4.  kendo.fx.js (optional for animation)
5.  kendo.draganddrop.js (if drag &amp; drop enabled)
6.  kendo.treeview.js


### Upload

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.upload.js


### Validator

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.validator.js


### Window

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (optional for animation)
4.  kendo.draganddrop.js
5.  kendo.resizable.js
6.  kendo.window.js


### Mobile Application

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.scroller.js
8.  kendo.mobile.application.js


### Mobile Button

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.button.js


### Mobile ButtonGroup

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.buttongroup.js


### Mobile ListView

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.js
4.  kendo.data.odata.js
5.  kendo.data.xml.js
6.  kendo.model.js
7.  kendo.history.js
8.  kendo.fx.js
9.  kendo.draganddrop.js
10.  kendo.mobile.view.js
11.  kendo.mobile.application.js
12.  kendo.mobile.scroller.js
13.  kendo.mobile.listview.js


### Mobile NavBar

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.navbar.js


### Mobile Scroller

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.scroller.js


### Mobile ScrollView

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.scrollview.js


### Mobile Switch

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.switch.js


### Mobile TabStrip

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.tabstrip.js

