---
title: Javascript Dependencies
slug: gs-javascript-dependencies
publish: true
---

### JavaScript files used by Kendo UI

Every widget from **Kendo UI** needs its JavaScript files to be included in order to work properly
This help topic lists the JavaScript files required by each widget.

### Combined Scripts

The following combined scripts are made available in order to simplify development and deployment.

*   **kendo.all.min.js** contains a minified version of all scripts (Web, DataViz and Mobile).
 **That file is available only in the Kendo Complete package**.
 *   **kendo.web.min.js** contains a minified version of all scripts from Kendo UI Web.
 *   **kendo.dataviz.min.js** contains a minified version of all scripts from Kendo UI DataViz.
 *   **kendo.mobile.min.js** contains a minified version of all scripts from Kendo UI Mobile.

 **Important:** Only one of the above scripts can be included at a time.

### Custom Combined Scripts

Users who own a commercial license can use the [custom download builder tool](http://www.kendoui.com/custom-download)
to create a single JavaScript file which contains only the required widgets and features.

### CDN

The minified versions of all JavaScript files (except jQuery) are also available via CDN

    http://cdn.kendostatic.com/<version>/js/<filename>.min.js
    
**e.g.** http://cdn.kendostatic.com/2011.3.1129/js/kendo.all.min.js

**Important:** in order to use HTTPS, you need to directly access the CloudFront CDN:

    https://da7xgjtj801h2.cloudfront.net/<version>/js/<filename>.min.js

### Individual scripts

If more granular control is required, the following separate script files, either minified or not,
can be included per widget basis.


<a name="autocomplete">AutoComplete</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js
7.  kendo.fx.js (if animation is enabled)
8.  kendo.popup.js
9.  kendo.list.js
10.  kendo.autocomplete.js


<a name="calendar">Calendar</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (if animation is enabled)
4.  kendo.calendar.js

<a name="chart">Chart</a>

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


<a name="combobox">ComboBox</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js
7.  kendo.fx.js (if animation is enabled)
8.  kendo.popup.js
9.  kendo.list.js
10.  kendo.combobox.js


<a name="datasource">DataSource</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML or editing)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js


<a name="datepicker">DatePicker</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (if animation is enabled)
4.  kendo.popup.js
5.  kendo.calendar.js
6.  kendo.datepicker.js


<a name="dragdrop">Drag and Drop</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.draganddrop.js


<a name="dropdownlist">DropDownList</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js
7.  kendo.fx.js (if animation is enabled)
8.  kendo.popup.js
9.  kendo.list.js
10.  kendo.dropdownlist.js


<a name="editor">Editor</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.popup.js
4.  kendo.list.js
5.  kendo.dropdownlist.js
6.  kendo.combobox.js
7.  kendo.fx.js (if animation is enabled)
8.  kendo.draganddrop.js (if popups are draggable and/or resizable)
9.  kendo.window.js
10.  kendo.editor.js


<a name="gauge">Gauge</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.js (if using MVVM)
4.  kendo.binder.js (if using MVVM)
5.  kendo.dataviz.core.js
6.  kendo.dataviz.vml.js
7.  kendo.dataviz.svg.js
8.  kendo.dataviz.gauge.js


<a name="grid">Grid</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.data.xml.js (if binding to XML)
5.  kendo.data.js
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


<a name="listview">ListView</a>

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


<a name="menu">Menu</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.popup.js
5.  kendo.menu.js


<a name="numerictextbox">NumericTextBox</a> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.numerictextbox.js


<a name="panelbar">PanelBar</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.panelbar.js


<a name="slider">Slider and RangeSlider</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.binder.js (if using MVVM)
4.  kendo.draganddrop.js
5.  kendo.slider.js


<a name="splitter">Splitter</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.draganddrop.js
5.  kendo.resizable.js
6.  kendo.splitter.js


<a name="tabstrip">TabStrip</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.js
4.  kendo.fx.js
5.  kendo.tabstrip.js


<a name="timepicker">TimePicker</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.popup.js
5.  kendo.timepicker.js


<a name="treeview">TreeView</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.draganddrop.js (if drag &amp; drop enabled)
5.  kendo.treeview.js


<a name="upload">Upload</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.upload.js


<a name="validator">Validator</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.validator.js


<a name="window">Window</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.draganddrop.js
5.  kendo.resizable.js
6.  kendo.window.js


<a name="mobile.application">Mobile Application</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.scroller.js
8.  kendo.mobile.application.js


<a name="mobile.button">Mobile Button</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.button.js


<a name="mobile.button-group">Mobile ButtonGroup</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.buttongroup.js


<a name="mobile.list-view">Mobile ListView</a>

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


<a name="mobile.nav-bar">Mobile NavBar</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.navbar.js


<a name="mobile.scroller">Mobile Scroller</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.scroller.js


<a name="mobile.scroll-view">Mobile ScrollView</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.scrollview.js


<a name="mobile.switch">Mobile Switch</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.switch.js


<a name="mobile.tab-strip">Mobile TabStrip</a>

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.tabstrip.js

