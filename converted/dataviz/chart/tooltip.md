---
title: Tooltip
publish: true
---

## Tooltip 

The Chart can display details about the data point that the mouse is currently hovering. The border of this tooltip matches the color of the series.

![](/Libraries/Documentation/chart-tooltip.sflb.ashx)

### Configuration

The tooltip is not visible by default. You can enable it by setting the visible property of the tooltip object to true:

 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`$(``"#chart"``).kendoChart({`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`series: [{`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`type: ``"bar"``,`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`name: ``"United States"``,`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`data: [67.96, 68.93, 75, 74, 78]`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`}],`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`categoryAxis: {`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`categories: [2005, 2006, 2007, 2008, 2009]`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`},`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`**tooltip: {**`</span></span></div> <div style="background-color: #ffffff;"><span>**`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`visible: ``true`</span>**</span></div> <div style="background-color: #f8f8f8;"><span>**`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`}`</span>**</span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`});`</span></span></div> </div> 

&nbsp;The tooltip can also be configured per-series: 
 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`series: [{`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`type: ``"bar"``,`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`name: ``"United States"``,`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`data: [67.96, 68.93, 75, 74, 78],`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`**tooltip: {**`</span></span></div> <div style="background-color: #f8f8f8;"><span>**`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;"><span><span style="margin-left: 12px ! important;">`visible: ``true`</span></span></span>**</span></div> <div style="background-color: #ffffff;"><span>**`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`}`</span>**</span></div> <div style="background-color: #f8f8f8;"><span><span style="margin-left: 0px ! important;">`}]`</span></span></div> </div> 

### 

### Formating values

The point value can be formatted using the format property:

 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`tooltip: {`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`visible: ``true``,`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`format: ``"Value: {0:N0}"`</span></span></div> <div style="background-color: #f8f8f8;"><span><span style="margin-left: 0px ! important;">`}`</span></span></div> </div> 

The format string supports a subset of the syntax available in Java&nbsp;and&nbsp;C#.

Here "N0" indicates that the value should be rounded to a whole number and should have a thousands separator.

**Note: **Points in&nbsp;XY charts have two values - {0} and {1} (X and Y).

### Templates

Tooltip content can be defined with a [template](http://www.kendoui.com/documentation/framework/templates/overview.aspx)&nbsp;when more flexibility is desired. The template provides access to all information associated with the point:

*   value - the point value. Value dimensions are available as properties, for example,&nbsp;**value.x** and **value.y**
*   category - the category name.
*   series - the data series.
*   dataItem - the original data item (when binding to dataSource). <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`$(``"#chart"``).kendoChart({`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 15px ! important;">`title: {`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 27px ! important;">`text: ``"My Chart Title"`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 15px ! important;">`},`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 15px ! important;">`series: [{`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 27px ! important;">`name: ``"Series 1"``,`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 27px ! important;">`data: [200, 450, 300, 125]`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 15px ! important;">`}],`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 15px ! important;">`categoryAxis: {`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 27px ! important;">`categories: [2000, 2001, 2002, 2003]`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 15px ! important;">`},`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 15px ! important;">`tooltip: {`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 27px ! important;">`visible: ``true``,`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 27px ! important;">**`template: ``"${category} - ${value}"`**</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 15px ! important;">`}`</span></span></div> <div style="background-color: #f8f8f8;"><span><span style="margin-left: 0px ! important;">`});`</span></span></div> </div> 

## See also

Refer to the [Configuration section](http://www.kendoui.com/documentation/dataviz/chart/configuration.aspx) for a full list of configuration options.