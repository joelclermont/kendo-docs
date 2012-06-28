---
title: Javascript Dependencies
publish: true
---

### JavaScript files used by Kendo UI

Every widget from **Kendo UI** needs its JavaScript files to be included in order to work properly. This help topic lists the JavaScript files required by each widget.

### Combined Scripts

The following combined scripts are made available in order to simplify development and deployment.

*   **kendo.all.min.js** contains a minified version of all scripts (Web, DataViz and Mobile).
 **That file is available only in the Kendo Complete package**.
*   **kendo.web.min.js** contains a minified version of all scripts from Kendo UI Web.
*   **kendo.dataviz.min.js**&nbsp;contains a minified version of all scripts from Kendo UI DataViz.&nbsp;
*   **kendo.mobile.min.js**&nbsp;contains a minified version of all scripts from Kendo UI Mobile.&nbsp; 

**Important:** Only one of the above scripts can be included at a time.

### Custom Combined Scripts

Users who own a commercial license can use the [custom download builder tool](http://www.kendoui.com/custom-download) to create a single JavaScript file which contains only the required widgets and features.

### CDN

The minified versions of all JavaScript files (except jQuery) are also available via CDN
 <pre>http://cdn.kendostatic.com/&lt;version&gt;/js/&lt;filename&gt;.min.js </pre> 

**e.g.** http://cdn.kendostatic.com/2011.3.1129/js/kendo.all.min.js
 **Important:** in order to use HTTPS at this point, you need to directly access the CloudFront CDN:
<pre>[https://da7xgjtj801h2.cloudfront.net/&lt;version&gt;/js/&lt;filename&gt;.min.js](https://da7xgjtj801h2.cloudfront.net/&lt;version&gt;/js/&lt;filename&gt;.min.js)&nbsp;</pre> 

### Individual scripts

If more granular control is required, the following separate script files, either minified or not, can be included per widget basis.
 <dl> <dt><a name="autocomplete" target="blank" re_target="blank">**AutoComplete**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js
7.  kendo.fx.js (if animation is enabled)
8.  kendo.popup.js
9.  kendo.list.js
10.  kendo.autocomplete.js </dd> <dt><a name="calendar" target="blank" re_target="blank">**Calendar**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (if animation is enabled)
4.  kendo.calendar.js </dd> <dt><a name="chart" target="blank" re_target="blank">**Chart**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.data.xml.js (if binding to XML)
5.  kendo.data.js
6.  <span>kendo.binder.js (if using MVVM)</span>
7.  kendo.dataviz.core.js
8.  kendo.dataviz.vml.js
9.  kendo.dataviz.svg.js
10.  kendo.dataviz.chart.js </dd> <dt><a name="combobox" target="blank" re_target="blank">**ComboBox**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js
7.  kendo.fx.js (if animation is enabled)
8.  kendo.popup.js
9.  kendo.list.js
10.  kendo.combobox.js </dd> <dt><a name="datasource" target="blank" re_target="blank">**DataSource**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML or editing)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js </dd> <dt><a name="datepicker" target="blank" re_target="blank">**DatePicker**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js (if animation is enabled)
4.  kendo.popup.js
5.  kendo.calendar.js
6.  kendo.datepicker.js </dd> <dt><a name="dragdrop" target="blank" re_target="blank">**Drag and Drop**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.draganddrop.js </dd> <dt><a name="dropdownlist" target="blank" re_target="blank">**DropDownList**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.odata.js (if binding to OData)
4.  kendo.model.js (if binding to XML)
5.  kendo.data.xml.js (if binding to XML)
6.  kendo.data.js
7.  kendo.fx.js (if animation is enabled)
8.  kendo.popup.js
9.  kendo.list.js
10.  kendo.dropdownlist.js </dd> <dt><a name="gauge" target="blank" re_target="blank">**Gauge**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.js (if using MVVM)
4.  kendo.binder.js (if using MVVM)
5.  kendo.dataviz.core.js
6.  kendo.dataviz.vml.js
7.  kendo.dataviz.svg.js
8.  kendo.dataviz.gauge.js </dd> <dt><a name="grid" target="blank" re_target="blank">**Grid**</a></dt> <dd> 

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
23.  kendo.grid.js </dd> <dt><a name="listview" target="blank" re_target="blank">**ListView**</a></dt> <dd> 

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
11.  kendo.listview.js </dd> <dt><a name="menu" target="blank" re_target="blank">**Menu**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.popup.js
5.  kendo.menu.js </dd> <dt><a name="numerictextbox" target="blank" re_target="blank">**NumericTextBox**</a> </dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.numerictextbox.js </dd> <dt><a name="panelbar" target="blank" re_target="blank">**PanelBar**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.panelbar.js </dd> <dt><a name="slider" target="blank" re_target="blank">**Slider and RangeSlider**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.binder.js (if using MVVM)
4.  kendo.draganddrop.js
5.  kendo.slider.js </dd> <dt><a name="splitter" target="blank" re_target="blank">**Splitter**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.draganddrop.js
5.  kendo.resizable.js
6.  kendo.splitter.js </dd> <dt><a name="tabstrip" target="blank" re_target="blank">**TabStrip**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.data.js
4.  kendo.fx.js
5.  kendo.tabstrip.js </dd> <dt><a name="timepicker" target="blank" re_target="blank">**TimePicker**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.popup.js
5.  kendo.timepicker.js </dd> <dt><a name="treeview" target="blank" re_target="blank">**TreeView**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.draganddrop.js (if drag &amp; drop enabled)
5.  kendo.treeview.js </dd> <dt><a name="upload" target="blank" re_target="blank">**Upload**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.upload.js </dd> <dt><a name="validator" target="blank" re_target="blank">**Validator**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.validator.js </dd> <dd></dd> <dt><a name="window" target="blank" re_target="blank">**Window**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.fx.js
4.  kendo.draganddrop.js
5.  kendo.resizable.js
6.  kendo.window.js </dd> <dt><a name="mobile.application" target="blank" re_target="blank">**Mobile Application**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.scroller.js
8.  kendo.mobile.application.js </dd> <dt><a name="mobile.button" target="blank" re_target="blank">**Mobile Button**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.button.js </dd> <dt><a name="mobile.button-group" target="blank" re_target="blank">**Mobile ButtonGroup**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.buttongroup.js </dd> <dt><a name="mobile.list-view" target="blank" re_target="blank">**Mobile ListView**</a></dt> <dd> 

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
13.  kendo.mobile.listview.js </dd> <dt><a name="mobile.nav-bar" target="blank" re_target="blank">**Mobile NavBar**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.navbar.js </dd> <dt><a name="mobile.scroller" target="blank" re_target="blank">**Mobile Scroller**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.scroller.js </dd> <dt><a name="mobile.scroll-view" target="blank" re_target="blank">**Mobile ScrollView**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.scrollview.js </dd> <dt><a name="mobile.switch" target="blank" re_target="blank">**Mobile Switch**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.switch.js </dd> <dt><a name="mobile.tab-strip" target="blank" re_target="blank">**Mobile TabStrip**</a></dt> <dd> 

1.  jquery-1.7.1.js
2.  kendo.core.js
3.  kendo.history.js
4.  kendo.fx.js
5.  kendo.draganddrop.js
6.  kendo.mobile.view.js
7.  kendo.mobile.application.js
8.  kendo.mobile.scroller.js
9.  kendo.mobile.tabstrip.js </dd> </dl>