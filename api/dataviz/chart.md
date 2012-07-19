---
title: kendo.dataviz.ui.Chart
slug: dataviz-kendo.dataviz.ui.chart
tags: api,dataviz
publish: true
---

# kendo.dataviz.ui.Chart

## Configuration

### axisDefaults `Object`

Default options for all chart axes.

### categoryAxis `Object`

The category axis configuration options.

### categoryAxis.axisCrossingValue `Number`*(default: 0)*

Category index at which the first value axis crosses this axis.

### categoryAxis.axisCrossingValue `Array`*(default: [0])*

Category indicies at which the value axes cross the category axis.

**Note:&nbsp;** Specify an index greater than or equal to the number
of categories to denote the far end of the axis.

#### Example
    <p>
    $("#chart").kendoChart({
         categoryAxis: {
             categories: ["A", "B"]
                 axisCrossingValue: [0, 100]
             },
         valueAxis: [{ }, { name: "secondary" }],
         ...
    })'
    </p>

### categoryAxis.categories `Array`

Array of category names.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            categories: [ 2005, 2006, 2007, 2008, 2009 ]
        },
        ...
    });

### categoryAxis.color `String`

Color to apply to all axis elements. Any valid CSS color string will work here, including hex and rgb.
Individual color settings for line and labels take priority.

### categoryAxis.field `String`

The data field containing the category name.

#### Example

    // assuming the following data...
    var data = [ { sales: 200, year: 2005 }, { sales: 300, year: 2006 }, { sales: 400, year: 2007 }];
    // specify the "year" as the field for the category axis
    $("#chart").kendoChart({
        ...,
        categoryAxis: {
            field: "year"
        },
        ...
    });

### categoryAxis.labels `Object`

Configures the axis labels.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            labels: {
                // set the background color of the labels to a light grey
                background: "#e2e2e2",
                // rotate the labels just slightly for visual effect
                rotation: 10,
                // format the labels for currency
                format: "C"
            }
        },
        ...
    });

### categoryAxis.labels.background `String`

The background color of the labels. Any valid CSS color string will work here, including hex
and rgb.

### categoryAxis.labels.border `Object`

The border of the labels.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            labels: {
                border: {
                    // make the width 1
                    width: 1,
                    // set the color to a dark blue
                    color: "#336699",
                    // set the border style to dashed
                    dashType: "dash"
                }
            }
        },
        ...
    });

### categoryAxis.labels.border.color `String`*(default: "black")*

 The color of the border. Any valid CSS color string will work here, including hex and rgb.

### categoryAxis.labels.border.dashType `String`*(default: "solid")*

The dash type of the border.

#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### categoryAxis.labels.border.width `Number`*(default: 0)*

 The width of the border.

### categoryAxis.labels.color `String`

The text color of the labels. Any valid CSS color string will work here, including hex and rgb.

### categoryAxis.labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            labels: {
                // make the font 14px
                font: "14px Arial,Helvetica,sans-serif"
            }
        },
        ...
    });

### categoryAxis.labels.format `String`

The format of the labels.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
           labels: {
               // set the format to currency
               format: "C"
           }
        },
        ...
    });

### categoryAxis.labels.margin `Number | Object`*(default: 0)*

 The margin of the labels.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            label: {
                // sets the top, right, bottom and left margin to 3px.
                margin: 3
            }
        },
        ...
    });
    //
    $("#chart").kendoChart({
        categoryAxis: {
            label: {
                // sets the top and left margin to 1px
                // margin right and bottom are with 0px (by default)
                margin: { top: 1, left: 1 }
            }
        },
        ...
    });

### categoryAxis.labels.mirror `Boolean`

Mirrors the axis labels and ticks.
If the labels are normally on the left side of the axis,
mirroring the axis will render them to the right.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            labels: {
                // mirror the labels on the right
                mirror: true
            }
        },
        ...
    });

### categoryAxis.labels.padding `Number | Object`*(default: 0)*

The padding of the labels.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            label: {
                // sets the top, right, bottom and left padding to 3px.
                padding: 3
            }
        },
        ...
    });
    //
    $("#chart").kendoChart({
        categoryAxis: {
            label: {
                // sets the top and left padding to 1px
                // padding right and bottom are with 0px (by default)
                padding: { top: 1, left: 1 }
            }
        },
        ...
    });

### categoryAxis.labels.rotation `Number`*(default: 0)*

 The rotation angle of the labels.

### categoryAxis.labels.skip `Number`*(default: 1)*

 Number of labels to skip.
Skips rendering the first n labels.

### categoryAxis.labels.step `Number`*(default: 1)*

 Label rendering step.
Every n-th label is rendered where n is the step

### categoryAxis.labels.template `String/Function`

The label template.
Template variables:


*   **value** - the value

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [{
                 name: "Series 1",
                 data: [200, 450, 300, 125]
         }],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003],
             labels: {
                 // labels template
                 template: "Year: #= value #"
             }
         }
    });

### categoryAxis.labels.visible `Boolean`*(default: true)*

 The visibility of the labels.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            labels: {
                // hide the lables
                visible: false
            }
        },
        ...
    });

### categoryAxis.line `Object`

Configures the axis line. This will also effect major and minor ticks, but not gridlines.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            line: {
                // change the line width to 2 pixels
                width: 2,
                // set the color to light grey
                color: "#e2e2e2"
            }
        },
        ...
    });

### categoryAxis.line.color `String`*(default: "black")*

 The color of the lines. Any valid CSS color string will work here, including hex and rgb.


**Note:** This will also effect the major and minor ticks, but not the grid lines.

### categoryAxis.line.dashType `String`*(default: "solid")*

The dash type of the line.

#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### categoryAxis.line.visible `Boolean`*(default: true)*

 The visibility of the lines.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            line: {
                // hide the lines completely
                visible: false
            }
        },
        ...
    });

### categoryAxis.line.width `Number`*(default: 1)*

 The width of the line. This will also effect the major and minor ticks, but
not the grid lines.

### categoryAxis.majorGridLines `Object`

Configures the major grid lines. These are the lines that are an extension of the major ticks through the
body of the chart.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
             majorGridLines: {
                // set the width of the lines to 2 pixels
                width: 2,
                // set the color to a dark blue
                color: "#336699"
            }
        },
        ...
    });

### categoryAxis.majorGridLines.color `String`*(default: "black")*

 The color of the lines. Any valid CSS color string will work here, including hex and rgb.

### categoryAxis.majorGridLines.dashType `String`*(default: "solid")*

The dash type of the grid lines.

#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### categoryAxis.majorGridLines.visible `Boolean`*(default: false)*

 The visibility of the lines.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            majorGridLines: {
                // hide the major grid lines
                visible: false
            }
        },
        ...
    });

### categoryAxis.majorGridLines.width `Number`*(default: 1)*

 The width of the lines.

### categoryAxis.majorTicks `Object`

The major ticks of the axis.

### categoryAxis.majorTicks.size `Number`*(default: 4)*

 The axis major tick size. This is the length of the line in pixels that is drawn to indicate the tick
on the chart.

### categoryAxis.majorTicks.visible `Boolean`*(default: true)*

 The visibility of the major ticks.

### categoryAxis.minorGridLines `Object`

Configures the minor grid lines.  These are the lines that are an extension of the minor ticks through
the body of the chart.

Note that minor grid lines are not visible by default, therefore none of these settings will take effect with the minor grid
lines visibility being set to **true**
.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            minorGridLines: {
                // set visible to true
                visible: true,
                // set width to 2 pixels
                width: 2,
                // set the color to a dark blue
                color: "#336699"
            }
        },
        ...
    });

### categoryAxis.minorGridLines.color `String`*(default: "black")*

 The color of the lines. Any valid CSS color string will work here, including hex and
rgb.

Note that this setting has no effect if the visibility of the minor
grid lines is not set to **true**.

### categoryAxis.minorGridLines.dashType `String`*(default: "solid")*

The dash type of the grid lines.

#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### categoryAxis.minorGridLines.visible `Boolean`*(default: false)*

 The visibility of the lines.

### categoryAxis.minorGridLines.width `Number`*(default: 1> The width of the lines. <p)*

 The width of the lines.

Note that this setting has no effect if the visibility of the minor
grid lines is not set to **true**.

### categoryAxis.minorTicks `Object`

The minor ticks of the axis.

### categoryAxis.minorTicks.size `Number`*(default: 3)*

 The axis minor tick size. This is the length of the line in pixels that is drawn to indicate the tick
on the chart.

### categoryAxis.minorTicks.visible `Boolean`*(default: false)*

 The visibility of the minor ticks.

### categoryAxis.name `Object`*(default: primary)*

 The unique axis name.

### categoryAxis.plotBands `Array`

The plot bands of category axis.
The plot band fields:


#### *"from"*

The start position of the plot band.

#### *"to"*

The end position of the plot band.

#### *"color"*

The color of the plot band.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            plotBands: [{
                from: 0.2,
                to: 0.4,
                color: "green"
            }]
        },
     });

### categoryAxis.reverse `Boolean`*(default: false)*

 Reverses the axis direction -
categories are listed from right to left and from top to bottom.

### categoryAxis.title `Object`

The title of the category axis.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            title: {
                // set the text of the title
                text: "Sales By District",
                // decreate the font size of the title to 14 px
                font: "14px Arial,Helvetica,sans-serif",
                // move the title to the bottom
                position: "bottom"
            }
        },
        ...
    });

### categoryAxis.title.background `String`

The background color of the title. Any valid CSS color string will work here, including
hex and rgb.

### categoryAxis.title.border `Object`

The border of the title.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            title: {
                // tweak the border around the title
                border: {
                    // set the width to 1
                    width: 1,
                    // set the color to a dark blue
                    color: "#336699",
                    // set the style to dashed
                    dashType: "dash"
                }
            }
        },
        ...
    });

### categoryAxis.title.border.color `String`*(default: "black")*

 The color of the border. Any valid CSS color string will work here, including
hex and rgb.

### categoryAxis.title.border.dashType `String`*(default: "solid")*

The dash type of the border.

#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

#### Example



### categoryAxis.title.border.width `Number`*(default: 0)*

 The width of the border.

### categoryAxis.title.color `String`

The text color of the title. Any valid CSS color string will work here, including hex and rgb.

### categoryAxis.title.font `String`*(default: "16px Arial,Helvetica,sans-serif")*

The font style of the title.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            title: {
                // decreate the font size of the title to 14 px
                font: "14px Arial,Helvetica,sans-serif"
            }
        }
        ...
    });

### categoryAxis.title.margin `Number|Object`*(default: 5)*

 The margin of the title.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            title: {
                // sets the top, right, bottom and left margin to 3px.
                margin: 3
            }
        },
        ...
    });
    //
    $("#chart").kendoChart({
        categoryAxis: {
            title: {
                // sets the top and left margin to 1px
                // margin right and bottom are with 0px (by default)
                margin: { top: 1, left: 1 }
            }
        },
        ...
    });

### categoryAxis.title.position `String`*(default: "center")*

 The position of the title.


#### *"top"*

The axis title is positioned on the top (applicable to vertical axis)

#### *"bottom"*

The axis title is positioned on the bottom (applicable to vertical axis)

#### *"left"*

The axis title is positioned on the left (applicable to horizontal axis)

#### *"right"*

The axis title is positioned on the right (applicable to horizontal axis)

#### *"center"*

The axis title is positioned in the center

### categoryAxis.title.rotation `Number`*(default: 0)*

 The rotation angle of the title.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            title: {
                // rotate the title 20 degrees
                rotate: 20
            }
        },
        ...
    });

### categoryAxis.title.text `String`

The text of the title.

### categoryAxis.title.visible `Boolean`*(default: true)*

 The visibility of the title.

#### Example

    $("#chart").kendoChart({
        categoryAxis: {
            title: {
                // hide the title
                visible: false
            }
        },
        ...
    });

### categoryAxis.type `String`*(default: "Category")*

 The axis type.


#### *"Category"*

Discrete category axis.

#### *"Date"*

Specialized axis for displaying chronological data.

### categoryAxis.type: "Date"

Properties specific to the date-time value axis.


Note: The Chart will automatically switch to a date category axis if the categories
are of type Date. Specify type explicitly when such behavior is undesired.

### categoryAxis.type: "Date".baseUnit `String`

The base time interval for the axis.
The default baseUnit is determined automatically from the minimum difference
between subsequent categories. Available options:

* minutes
* hours
* days
* months
* years

Series data is aggregated for the specified base unit by using the
**series.aggregate** function.

### categoryAxis.type: "Date".labels `Object`

Label settings specific to the date axis.

### categoryAxis.type: "Date".labels.culture `String`*(default: global culture)*

Culture to use for formatting the dates. See [Globalization](http://www.kendoui.com/documentation/framework/globalization/overview.aspx) for more information.

### categoryAxis.type: "Date".labels.dateFormats `Object`

Date format strings


#### *"hours"*

"HH:mm"

#### *"days"*

"M/d"

#### *"months"*

"MMM 'yy"

#### *"years"*

"yyyy"
The Chart will choose the appropriate format for the current `baseUnit`.
Setting the labels **format** option will override these defaults.

### categoryAxis.type: "Date".max `Number`

The last date displayed on the axis.
By default, the minimum date is the same as the last category.
This is often used in combination with the **min** configuration option to
set up a fixed date range.

### categoryAxis.type: "Date".min `Number`

The first date displayed on the axis.
By default, the minimum date is the same as the first category.
This is often used in combination with the **max** configuration option to
set up a fixed date range.

### categoryAxis.visible `Boolean`*(default: true)*

The visibility of the axis.

### chartArea `Object`

The chart area configuration options.
This is the entire visible area of the chart.

### chartArea.background `String`*(default: "white")*

The background color of the chart area.

### chartArea.border `Object`

The border of the chart area.

### chartArea.border.color `String`*(default: "black")*

The color of the border.

### chartArea.border.dashType `String`*(default: "solid")*

The dash type of the border.

#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### chartArea.border.width `Number`*(default: 0)*

 The width of the border.

### chartArea.height `Number`*(default: 400)*

 The height of the chart area.

### chartArea.margin `Number|Object`*(default: 5)*

 The margin of the chart area.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and left margin to 1px
    // margin right and bottom are with 5px (by default)
    margin: { top: 1, left: 1 }

### chartArea.width `Number`*(default: 600)*

 The width of the chart area.

### dataSource `Object`

DataSource configuration or instance.

#### Example

    $("#chart").kendoChart({
        dataSource: {
            transport: {
                 read: "spain-electricity.json"
            }
        },
        series: [{
            field: "value"
        }],
        categoryAxis: {
            field: "year"
        }
    });

    // Alternative configuration
    var dataSource = new kendo.data.DataSource({
        transport: {
             read: "spain-electricity.json"
        }
    });

    $("#chart").kendoChart({
        dataSource: dataSource,
        series: [{
            field: "value"
        }],
        categoryAxis: {
            field: "year"
        }
    });

### legend `Object`

The chart legend configuration options.

#### Example

    $("#chart").kendoChart({
        legend: {
            // set the background color to a dark blue
            background: "#336699",
            labels: {
                // set the font to a size of 14px
                font: "14px Arial,Helvetica,sans-serif",
                // set the color to red
                color: "red"
            },
            // move the legend to the left
            position: "left",
            // move the legend a bit closer to the chart by setting the x offset to 20
            offsetX: 20,
            // move the legend up to the top by setting the y offset to -100
            offsetY: -100,
        }
    });

### legend.background `String`*(default: "white")*

 The background color of the legend. Any valid CSS color string will work here, including hex and rgb.

### legend.border `Object`

The border of the legend.

#### Example

    $("#chart").kendoChart({
        legend: {
            border: {
                // set the border width to 2 pixels
                width: 2,
                // set the color to grey
                color: "grey",
                // set the dash type to solid. this is the default so we could leave this line out.
                dashType: "solid"
            }
        },
        ...
    });

### legend.border.color `String`*(default: "black")*

 The color of the border.

### legend.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

#### Example



### legend.border.width `Number`*(default: 0)*

 The width of the border.

### legend.labels `Object`

Configures the legend labels.

### legend.labels.color `String`*(default: "black")*

The color of the labels.
Any valid CSS color string will work here, including hex and rgb.

### legend.labels.font `String`*(default: 12px Arial,Helvetica,sans-serif)*

The font style of the labels.

### legend.labels.template `String`

The template of the labels.
Template variables:
*   **text** - the text the legend item.
*   **series** - the data series.
*   **value** - the point value. (only for donut and pie charts)
*   **percentage** - the point value represented as a percentage value. (only for donut and pie charts)
*   **dataItem** - the original data item used to construct the point. (only for donut and pie charts)


### legend.margin `Number | Object`*(default: 10)*

 The margin of the legend.

#### Example

    $("#chart").kendoChart({
        legend: {
            // sets the top, right, bottom and left margin to 3px.
            margin: 3
        },
        ...
    });
    //
    $("#chart").kendoChart({
        legend: {
            // sets the top and left margin to 1px
            // margin right and bottom are with 10px (by default)
            margin: { top: 1, left: 1 }
        },
        ...
    });

### legend.offsetX `Number`*(default: 0)*

 The X offset from its position.  The offset is relative to the current position of the legend.
For instance, a value of 20 will move the legend 20 pixels to the right of it's initial position.  A negative value will move the legend
to the left of the current position.

#### Example

    $("#chart").kendoChart({
        legend: {
            // move the legend to the left side of the chart
            offsetX: 20
        },
        ...
    });

### legend.offsetY `Number`*(default: 0)*

 The Y offset from its position.  The offset is relative to the current position of the legend.
For instance, a value of 20 will move the legend 20 pixels down from it's initial position.  A negative value will move the legend
upwards from the current position.

#### Example

    $("#chart").kendoChart({
        legend: {
            // move the legend up 100 pixels
            offsetY: -100
        },
        ...
    });

### legend.padding `Number | Object`*(default: 5)*

 The padding of the legend.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    $("#chart").kendoChart({
        legend: {
            // sets the top, right, bottom and left padding to 3px.
            padding: 3
        },
        ...
    });
    //
    $("#chart").kendoChart({
        legend: {
           // sets the top and left padding to 1px
           // padding right and bottom are with 5px (by default)
           padding: { top: 1, left: 1 }
        },
        ...
    });

### legend.position `String`*(default: right)*

 The positions of the legend.


#### *"top"*

The legend is positioned on the top.

#### *"bottom"*

The legend is positioned on the bottom.

#### *"left"*

The legend is positioned on the left.

#### *"right"*

The legend is positioned on the right.

#### *"custom"*

The legend is positioned using OffsetX and OffsetY.

### legend.visible `Boolean`*(default: true)*

 The visibility of the legend.

#### Example

    $("#chart").kendoChart({
        legend: {
            // hide the legend
            visible: false
        },
        ...
    });

### plotArea `Object`

The plot area configuration options. This is the area containing the plotted series.

### plotArea.background `String`*(default: "white")*

 The background color of the plot area.

### plotArea.border `Object`

The border of the plot area.

### plotArea.border.color `String`*(default: "black")*

 The color of the border.

### plotArea.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### plotArea.border.width `Number`*(default: 0)*

 The width of the border.

### plotArea.margin `Number|Object`*(default: 5)*

 The margin of the plot area.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and left margin to 1px
    // margin right and bottom are with 5px (by default)
    margin: { top: 1, left: 1 }

### series `Array`

Array of series definitions.



The series type is determined by the value of the type field.
If a type value is missing, the type is assumed to be the one specified in seriesDefaults.



Each series type has a different set of options.

### series.data `Array`

Array of data points.

### series.field `String`

The data field containing the series value.

### series.groupNameTemplate `String`

Name template for auto-generated
series when binding to grouped data.
Template variables:


*   **series** - the series options
*   **group** - the data group
*   **group.field** - the name of the field used for grouping
*   **group.value** - the field value for this group.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         dataSource: {
             data: seriesData,
             group: {
                 field: "product",
                 dir: "desc"
             }
         },
         series: [{
                 type: "bar",
                 name: "Sales",
                 fiels: "sales",
                 groupNameTemplate: "#= series.name # for #= group.field # #= group.value #"
                 // Sales for product Bar,
                 // Sales for product Foo,
                 // etc.
             }
         ]
    });

### series.name `String`

The series name visible in the legend.

### series.type="area"

Available options for area series:

### series.type="area".aggregate `String`*(default: "max")*

 Aggregate function for date series.
This function is used when a category (an year, month, etc.) contains two or more points.
The function return value is displayed instead of the individual points.


#### *"max"*

The highest value for the date period.

#### *"min"*

The lowest value for the date period.

#### *"sum"*

The sum of all values for the date period.

#### *"count"*

The number of values for the date period.

#### *"avg"*

The average of all values for the date period.

#### *function (values, series)*

User-defined aggregate function.

### series.type="area".color `String`

The series base color.

### series.type="area".labels `Object`

Configures the series data labels.

### series.type="area".labels.background `String`

The background color of the labels.

### series.type="area".labels.border `Object`

The border of the labels.

### series.type="area".labels.border.color `String`*(default: "black")*

 The color of the border.

### series.type="area".labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="area".labels.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="area".labels.color `String`

The text color of the labels.

### series.type="area".labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.

### series.type="area".labels.format `String`

The format of the labels.

#### Example

    //sets format of the labels
    format: "C"

### series.type="area".labels.margin `Number|Object`*(default: { left: 5, right: 5})*

The margin of the labels.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and bottom margin to 1px
    // margin left and right are with 5px (by default)
    margin: { top: 1, bottom: 1 }

### series.type="area".labels.padding `Number|Object`*(default: 0)*

 The padding of the labels.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // padding right and bottom are with 0px (by default)
    padding: { top: 1, left: 1 }

### series.type="area".labels.position `String`*(default: "above")*

Defines the position of the area labels.


#### *"above"*

The label is positioned at the top of the area chart marker.

#### *"right"*

The label is positioned at the right of the area chart marker.

#### *"below"*

The label is positioned at the bottom of the area chart marker.

#### *"left"*

The label is positioned at the left of the area chart marker.

### series.type="area".labels.template `String/Function`

The label template.
Template variables:


*   **value** - the point value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "area",
                 name: "Series 1",
                 data: [200, 450, 300, 125],
                 labels: {
                     // label template
                     template: "#= value #%",
                     visible: true
                 }
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         }
    });

### series.type="area".labels.visible `Boolean`*(default: false)*

 The visibility of the labels.

### series.type="area".line `String`

The line of the area chart.

### series.type="area".line.color `String`

The line color of the area chart.

### series.type="area".line.opacity `Number`*(default: 1)*

 The line opacity of the area chart.

### series.type="area".line.width `String`*(default: 4)*

 The line width of the area chart.

### series.type="area".markers `Object`

Configures the area markers.

### series.type="area".markers.background `String`

The background color of the current series markers.

### series.type="area".markers.border `Object`

The border of the markers.

### series.type="area".markers.border.color `String`*(default: "black")*

 The color of the border.

### series.type="area".markers.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="area".markers.size `Number`*(default: 6)*

 The marker size.

### series.type="area".markers.type `String`*(default: "circle")*

Configures the markers shape type.


#### *"square"*

The marker shape is square.

#### *"triangle"*

The marker shape is triangle.

#### *"circle"*

The marker shape is circle.

### series.type="area".markers.visible `Boolean`*(default: false)*

 The markers visibility.

### series.type="area".missingValues `String`*(default: "gap")*

Configures the behavior for handling missing values in area series.


#### *"interpolate"*

The value is interpolated from neighboring points.

#### *"zero"*

The value is assumed to be zero.

#### *"gap"*

The line stops before the missing point and continues after it.

### series.type="area".name `String`

The series name.

### series.type="area".opacity `Number`*(default: 0.4)*

 The series opacity.

### series.type="area".stack `Boolean`*(default: false)*

A value indicating if the series should be stacked.

### series.type="area".tooltip `Object`

The data point tooltip configuration options.

### series.type="area".tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### series.type="area".tooltip.border `Object`

The border configuration options.

### series.type="area".tooltip.border.color `String`*(default: "black")*

 The color of the border.

### series.type="area".tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="area".tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### series.type="area".tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### series.type="area".tooltip.format `String`

The tooltip format.

#### Example

    //sets format of the tooltip
    format: "C"

### series.type="area".tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### series.type="area".tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value** - the point value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "area",
                 name: "Series 1",
                 data: [200, 450, 300, 125],
                 tooltip: {
                     visible: true,
                     template: "#= category # - #= value #"
                 }
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         }
    });

### series.type="area".tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### series.type="bar"

Available options for bar series:

### series.type="bar".aggregate `String`*(default: "max")*

 Aggregate function for date series.
This function is used when a category (an year, month, etc.) contains two or more points.
The function return value is displayed instead of the individual points.


#### *"max"*

The highest value for the date period.

#### *"min"*

The lowest value for the date period.

#### *"sum"*

The sum of all values for the date period.

#### *"count"*

The number of values for the date period.

#### *"avg"*

The average of all values for the date period.

#### *function (values, series)*

User-defined aggregate function.

### series.type="bar".axis `String`*(default: primary)*

 The name of the value axis to use.

### series.type="bar".border `Object`

The border of the series.

### series.type="bar".border.color `String`*(default: the color of the curren series)*

The color of the border.

### series.type="bar".border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="bar".border.width `Number`*(default: 1)*

 The width of the border.

### series.type="bar".color `String`

The series base color.

### series.type="bar".colorField `String`

The data field containing the bar color.

### series.type="bar".gap `Number`*(default: 1.5)*

 The distance between category clusters.

### series.type="bar".labels `Object`

Configures the series data labels.

### series.type="bar".labels.background `String`

The background color of the labels.

### series.type="bar".labels.border `Object`

The border of the labels.

### series.type="bar".labels.border.color `String`*(default: "black")*

 The color of the border.

### series.type="bar".labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="bar".labels.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="bar".labels.color `String`

The text color of the labels.

### series.type="bar".labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.

### series.type="bar".labels.format `String`

The format of the labels.

#### Example

    //sets format of the labels
    format: "C"

### series.type="bar".labels.margin `Number|Object`*(default: 2)*

 The margin of the labels.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and left margin to 1px
    // margin right and bottom are with 2px (by default)
    margin: { top: 1, left: 1 }

### series.type="bar".labels.padding `Number|Object`*(default: 2)*

 The padding of the labels.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // padding right and bottom are with 2px (by default)
    padding: { top: 1, left: 1 }

### series.type="bar".labels.position `String`*(default: "outsideEnd")*

Defines the position of the bar labels.


#### *"center"*

The label is positioned at the bar center.

#### *"insideEnd"*

The label is positioned inside, near the end of the bar.

#### *"insideBase"*

The label is positioned inside, near the base of the bar.

#### *"outsideEnd"*

The label is positioned outside, near the end of the bar.
             Not applicable for stacked bar series.

### series.type="bar".labels.template `String/Function`

The label template.
Template variables:


*   **value** - the point value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "bar",
                 name: "Series 1",
                 data: [200, 450, 300, 125],
                 labels: {
                     // label template
                     template: "#= value #%",
                     visible: true
                 }
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         }
    });

### series.type="bar".labels.visible `Boolean`*(default: false)*

 The visibility of the labels.

### series.type="bar".name `String`

The series name.

### series.type="bar".opacity `Number`*(default: 1)*

 The series opacity.

### series.type="bar".overlay `Object`

The effects overlay.

### series.type="bar".overlay.gradient `String`*(default: "glass")*

 The gradient name.


#### *"glass"*

The bars have glass effect overlay.

#### *"none"*

The bars have no effect overlay.

### series.type="bar".spacing `Number`*(default: 0.4)*

 Space between bars.

### series.type="bar".stack `Boolean`*(default: false)*

A value indicating if the series should be stacked.

### series.type="bar".stack `String`

Indicates that the series should be stacked in a group with the specified name.

### series.type="bar".tooltip `Object`

The data point tooltip configuration options.

### series.type="bar".tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### series.type="bar".tooltip.border `Object`

The border configuration options.

### series.type="bar".tooltip.border.color `String`*(default: "black")*

 The color of the border.

### series.type="bar".tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="bar".tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### series.type="bar".tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### series.type="bar".tooltip.format `String`

The tooltip format.

#### Example

    //sets format of the tooltip
    format: "C"

### series.type="bar".tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### series.type="bar".tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value** - the point value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "bar",
                 name: "Series 1",
                 data: [200, 450, 300, 125],
                 tooltip: {
                     visible: true,
                 template: "#= category # - #= value #"
                 }
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         }
    });

### series.type="bar".tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### series.type="bubble"

Available options for bubble series:

### series.type="bubble".border `Object`

The border of the bubble.

### series.type="bubble".border.color `String`*(default: "black")*

 The color of the border.

### series.type="bubble".border.width `Number`*(default: 0)*

 The width of the border.

### series.type="bubble".categoryField `String`

The data field containing the bubble category name.

### series.type="bubble".color `String`

The series base color.

### series.type="bubble".colorField `String`

The data field containing the bubble color.

### series.type="bubble".data `Array`

Array of data items (optional).
The bubble chart can be bound to an array of arrays with three numbers (X, Y and Size).


#### Example

    // ...
     series:[{
         type: "bubble",
         data:[[1, 1, 1], [1, 2, 2]],
         name: "Points"
     }]
     // ...

### series.type="bubble".labels `Object`

Configures the series data labels.

### series.type="bubble".labels.background `String`

The background color of the labels.

### series.type="bubble".labels.border `Object`

The border of the labels.

### series.type="bubble".labels.border.color `String`*(default: "black")*

 The color of the border.

### series.type="bubble".labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="bubble".labels.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="bubble".labels.color `String`

The text color of the labels.

### series.type="bubble".labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.

### series.type="bubble".labels.format `String`

The format of the labels.

#### Example

    //sets format of the labels
    format: "C"

### series.type="bubble".labels.margin `Number|Object`*(default: { left: 5, right: 5})*

The margin of the labels.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and bottom margin to 1px
    // margin left and right are with 5px (by default)
    margin: { top: 1, bottom: 1 }

### series.type="bubble".labels.padding `Number|Object`*(default: 0)*

 The padding of the labels.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // padding right and bottom are with 0px (by default)
    padding: { top: 1, left: 1 }

### series.type="bubble".labels.position `String`*(default: "above")*

Defines the position of the bubble labels.


#### *"above"*

The label is positioned at the top of the bubble chart marker.

#### *"right"*

The label is positioned at the right of the bubble chart marker.

#### *"below"*

The label is positioned at the bottom of the bubble chart marker.

#### *"left"*

The label is positioned at the left of the bubble chart marker.

### series.type="bubble".labels.template `String/Function`

The label template.
Template variables:


*   **value.x** - the x value
*   **value.y** - the y value
*   **value.size** - the size value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "bubble",
                 name: "Series 1",
                 data: [[1, 1, 1], [1, 2, 2], [1, 3, 3]],
                 labels: {
                     // label template
                     template: "#= value.x # - #= value.y # - #= value.size #",
                     visible: true
                 }
             }
         ]
    });

### series.type="bubble".labels.visible `Boolean`*(default: false)*

 The visibility of the labels.

### series.type="bubble".maxSize `Number`*(default: 100)*

 The max size of the bubble.

### series.type="bubble".minSize `Number`*(default: 5)*

 The min size of the bubble.

### series.type="bubble".name `String`

The series name.

### series.type="bubble".negativeValues `Object`

The settings for negative values.

### series.type="bubble".negativeValues.color `String`*(default: "#ffffff")*

 The color of the negative values.

### series.type="bubble".negativeValues.visible `Boolean`*(default: false)*

 The visibility of the negative values.

### series.type="bubble".opacity `Number`*(default: 0.6)*

 The series opacity.

### series.type="bubble".sizeField `String`

The data field containing the bubble size value.

### series.type="bubble".tooltip `Object`

The data point tooltip configuration options.

### series.type="bubble".tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### series.type="bubble".tooltip.border `Object`

The border configuration options.

### series.type="bubble".tooltip.border.color `String`*(default: "black")*

 The color of the border.

### series.type="bubble".tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="bubble".tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### series.type="bubble".tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### series.type="bubble".tooltip.format `String`

The tooltip format.
Format variables:


*   **0** - the x value
*   **1** - the y value
*   **2** - the size value
*   **3** - the category name

#### Example

    //sets format of the tooltip
    format: "{0:C}--{1:C}"

### series.type="bubble".tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### series.type="bubble".tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value.x** - the x value
*   **value.y** - the y value
*   **value.size** - the size value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "bubble",
                 name: "Series 1",
                 data: [[1, 1, 1], [1, 2, 2], [1, 3, 3]],
                 tooltip: {
                     visible: true,
                     template: "#= category # - #= value.x # - #= value.y # - #= value.size #"
                 }
             }
         ]
    });

### series.type="bubble".tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### series.type="bubble".visibleInLegendField `String`

A boolean value indicating whether to show the bubble category name in the legend.

### series.type="bubble".xAxis `String`*(default: primary)*

 The name of the X axis to use.

### series.type="bubble".xField `String`

The data field containing the bubble x value.

### series.type="bubble".yAxis `String`*(default: primary)*

 The name of the Y axis to use.

### series.type="bubble".yField `String`

The data field containing the bubble y value.

### series.type="column"

Column series accepts the same parameters as bar series.
The difference is that column series are rendered on a horizontal category axis.

### series.type="donut"

Available options for donut series:

### series.type="donut".border `Object`

The border of the series.

### series.type="donut".border.color `String`*(default: the color of the curren series)*

The color of the border.

### series.type="donut".border.dashType `String`*(default: solid)*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="donut".border.width `Number`*(default: 1)*

 The width of the border.

### series.type="donut".categoryField `String`

The data field containing the sector category name.

### series.type="donut".colorField `String`

The data field containing the sector color.

### series.type="donut".connectors `Object`

The label connectors options.

### series.type="donut".connectors.color `String`

The color of the connector line.

### series.type="donut".connectors.padding `Number`*(default: 4)*

The padding between the connector line and the label, and connector line and donut chart.

### series.type="donut".connectors.width `Number`*(default: 1)*

 The width of the connector line.

### series.type="donut".data `Array`

Array of data items (optional).
The donut chart can be bound to an array of numbers or an array of objects
with the following fields:


#### *"value"*

The sector value.

#### *"category"*

The sector category that is shown in the legend.

#### *"color"*

The sector color.

#### *"explode"*

A boolean value indicating whether to explode the sector(available only for the last level of the series).

#### *"visibleInLegend"*

A boolean value indicating whether to show the sector in the legend.


#### Example

    // ...
     series:[{
         type: "donut",
         data:[{
             value: 40,
             category: "Apples"
         }, {
             value: 60,
             category: "Oranges",
             color: "#ff6103"
         }],
         name: "Sales in Percent"
     }]
     // ...

### series.type="donut".explodeField `String`

The data field containing a boolean value that indicates if the sector is exploded
(available only for the last level of the series).

### series.type="donut".holeSize `Number`

The the size of the donut hole.

### series.type="donut".labels `Object`

Configures the series data labels.

### series.type="donut".labels.align `String`*(default: "circle")*

Defines the alignment of the donut labels.


#### *"circle"*

The labels are positioned in circle around the donut chart.

#### *"column"*

The labels are positioned in columns to the left and right of the donut chart.

### series.type="donut".labels.background `String`

The background color of the labels.

### series.type="donut".labels.border `Object`

The border of the labels.

### series.type="donut".labels.border.color `String`*(default: "black")*

 The color of the border.

### series.type="donut".labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="donut".labels.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="donut".labels.color `String`

The text color of the labels.

### series.type="donut".labels.distance `Number`*(default: 35)*

 The distance of the labels.

### series.type="donut".labels.font `String`*(default: "12px Arial, sans-serif")*

The font style of the labels.

### series.type="donut".labels.format `String`

The format of the labels.

#### Example

    //sets format of the labels
    format: "C"

### series.type="donut".labels.margin `Number|Object`*(default: 0.5)*

 The margin of the labels.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and left margin to 1px
    // margin right and bottom are with 2px (by default)
    margin: { top: 1, left: 1 }

### series.type="donut".labels.padding `Number|Object`*(default: 0)*

 The padding of the labels.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // padding right and bottom are with 2px (by default)
    padding: { top: 1, left: 1 }

### series.type="donut".labels.position `String`*(default: "center")*

Defines the position of the donut labels.


#### *"center"*

The labels are positioned at the center of the donut segments.

#### *"insideEnd"*

The labels are positioned inside, near the end of the donut segments.

#### *"outsideEnd"*

The labels are positioned outside, near the end of the donut segments.
             The labels and the donut segments are connected with connector line.

### series.type="donut".labels.template `String/Function`

The label template.
Template variables:


*   **value** - the point value
*   **percentage** - the point value represented as a percentage value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [{
             type: "donut",
             data: [
                 { value: 200, category: 2000 },
                 { value: 450, category: 2001 },
                 { value: 300, category: 2002 },
                 { value: 125, category: 2003 }
             ],
             labels: {
                 // label template
                 template: "#= value #%",
                 visible: true
             }
         }]
    });

### series.type="donut".labels.visible `Boolean`*(default: false)*

 The visibility of the labels.

### series.type="donut".margin `Number`*(default: 1)*

 The margin around each series
(not available for the last level of the series).

### series.type="donut".opacity `Number`*(default: 1)*

 The series opacity.

### series.type="donut".overlay `Object`

The effects overlay.

### series.type="donut".overlay.gradient `String`*(default: "roundedBevel")*

 The gradient name.
Available options are "none" and "roundedCircle".

### series.type="donut".padding `Number`

The padding around the donut chart (equal on all sides).

### series.type="donut".size `Number`

The size of the series.

### series.type="donut".startAngle `number`*(default: 90)*

 The start angle of the first donut segment.

### series.type="donut".tooltip `Object`

The data point tooltip configuration options.

### series.type="donut".tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### series.type="donut".tooltip.border `Object`

The border configuration options.

### series.type="donut".tooltip.border.color `String`*(default: "black")*

 The color of the border.

### series.type="donut".tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="donut".tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### series.type="donut".tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### series.type="donut".tooltip.format `String`

The tooltip format.

#### Example

    //sets format of the tooltip
    format: "C"

### series.type="donut".tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### series.type="donut".tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value** - the point value
*   **percentage** - the point value represented as a percentage value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [{
                 type: "donut",
                 name: "Series 1",
                 data: [200, 450, 300, 125],
                 tooltip: {
                     visible: true,
                     template: "#= category # - #= value #"
                 }
         }]
    });

### series.type="donut".tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### series.type="line"

Available options for line series:

### series.type="line".aggregate `String`*(default: "max")*

 Aggregate function for date series.
This function is used when a category (an year, month, etc.) contains two or more points.
The function return value is displayed instead of the individual points.


#### *"max"*

The highest value for the date period.

#### *"min"*

The lowest value for the date period.

#### *"sum"*

The sum of all values for the date period.

#### *"count"*

The number of values for the date period.

#### *"avg"*

The average of all values for the date period.

#### *function (values, series)*

User-defined aggregate function.

### series.type="line".axis `String`*(default: primary)*

 The name of the value axis to use.

### series.type="line".color `String`

The series base color.

### series.type="line".dashType `String`*(default: "solid")*

 The dash type of the line.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="line".labels `Object`

Configures the series data labels.

### series.type="line".labels.background `String`

The background color of the labels.

### series.type="line".labels.border `Object`

The border of the labels.

### series.type="line".labels.border.color `String`*(default: "black")*

 The color of the border.

### series.type="line".labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="line".labels.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="line".labels.color `String`

The text color of the labels.

### series.type="line".labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.

### series.type="line".labels.format `String`

The format of the labels.

#### Example

    //sets format of the labels
    format: "C"

### series.type="line".labels.margin `Number|Object`*(default: { left: 5, right: 5})*

The margin of the labels.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and bottom margin to 1px
    // margin left and right are with 5px (by default)
    margin: { top: 1, bottom: 1 }

### series.type="line".labels.padding `Number|Object`*(default: 0)*

 The padding of the labels.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // padding right and bottom are with 0px (by default)
    padding: { top: 1, left: 1 }

### series.type="line".labels.position `String`*(default: "above")*

Defines the position of the line labels.


#### *"above"*

The label is positioned at the top of the line chart marker.

#### *"right"*

The label is positioned at the right of the line chart marker.

#### *"below"*

The label is positioned at the bottom of the line chart marker.

#### *"left"*

The label is positioned at the left of the line chart marker.

### series.type="line".labels.template `String/Function`

The label template.
Template variables:


*   **value** - the point value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "line",
                 name: "Series 1",
                 data: [200, 450, 300, 125],
                 labels: {
                     // label template
                     template: "#= value #%",
                     visible: true
                 }
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         }
    });

### series.type="line".labels.visible `Boolean`*(default: false)*

 The visibility of the labels.

### series.type="line".markers `Object`

Configures the line markers.

### series.type="line".markers.background `String`

The background color of the current series markers.

### series.type="line".markers.border `Object`

The border of the markers.

### series.type="line".markers.border.color `String`*(default: "black")*

 The color of the border.

### series.type="line".markers.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="line".markers.size `Number`*(default: 6)*

 The marker size.

### series.type="line".markers.type `String`*(default: "circle")*

Configures the markers shape type.


#### *"square"*

The marker shape is square.

#### *"triangle"*

The marker shape is triangle.

#### *"circle"*

The marker shape is circle.

### series.type="line".markers.visible `Boolean`*(default: true)*

 The markers visibility.

### series.type="line".missingValues `String`*(default: "gap")*

Configures the behavior for handling missing values in line series.


#### *"interpolate"*

The value is interpolated from neighboring points.

#### *"zero"*

The value is assumed to be zero.

#### *"gap"*

The line stops before the missing point and continues after it.

### series.type="line".name `String`

The series name.

### series.type="line".opacity `Number`*(default: 1)*

 The series opacity.

### series.type="line".stack `Boolean`*(default: false)*

A value indicating if the series should be stacked.

### series.type="line".tooltip `Object`

The data point tooltip configuration options.

### series.type="line".tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### series.type="line".tooltip.border `Object`

The border configuration options.

### series.type="line".tooltip.border.color `String`*(default: "black")*

 The color of the border.

### series.type="line".tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="line".tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### series.type="line".tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### series.type="line".tooltip.format `String`

The tooltip format.

#### Example

    //sets format of the tooltip
    format: "C"

### series.type="line".tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### series.type="line".tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value** - the point value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "line",
                 name: "Series 1",
                 data: [200, 450, 300, 125],
                 tooltip: {
                     visible: true,
                     template: "#= category # - #= value #"
                 }
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         }
    });

### series.type="line".tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### series.type="line".width `String`*(default: 4)*

 The line width of the line chart.

### series.type="pie"

Available options for pie series:

### series.type="pie".border `Object`

The border of the series.

### series.type="pie".border.color `String`*(default: the color of the curren series)*

The color of the border.

### series.type="pie".border.dashType `String`*(default: solid)*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="pie".border.width `Number`*(default: 1)*

 The width of the border.

### series.type="pie".categoryField `String`

The data field containing the sector category name.

### series.type="pie".colorField `String`

The data field containing the sector color.

### series.type="pie".connectors `Object`

The label connectors options.

### series.type="pie".connectors.color `String`

The color of the connector line.

### series.type="pie".connectors.padding `Number`*(default: 4)*

The padding between the connector line and the label, and connector line and pie chart.

### series.type="pie".connectors.width `Number`*(default: 1)*

 The width of the connector line.

### series.type="pie".data `Array`

Array of data items (optional).
The pie chart can be bound to an array of numbers or an array of objects
with the following fields:


#### *"value"*

The sector value.

#### *"category"*

The sector category that is shown in the legend.

#### *"color"*

The sector color.

#### *"explode"*

A boolean value indicating whether to explode the sector.

#### *"visibleInLegend"*

A boolean value indicating whether to show the sector in the legend.


#### Example

    // ...
     series:[{
         type: "pie",
         data:[{
             value: 40,
             category: "Apples"
         }, {
             value: 60,
             category: "Oranges",
             color: "#ff6103"
             }
         ],
         name: "Sales in Percent"
     }]
     // ...

### series.type="pie".explodeField `String`

The data field containing a boolean value that indicates if the sector is exploded.

### series.type="pie".labels `Object`

Configures the series data labels.

### series.type="pie".labels.align `String`*(default: "circle")*

Defines the alignment of the pie labels.


#### *"circle"*

The labels are positioned in circle around the pie chart.

#### *"column"*

The labels are positioned in columns to the left and right of the pie chart.

### series.type="pie".labels.background `String`

The background color of the labels.

### series.type="pie".labels.border `Object`

The border of the labels.

### series.type="pie".labels.border.color `String`*(default: "black")*

 The color of the border.

### series.type="pie".labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="pie".labels.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="pie".labels.color `String`

The text color of the labels.

### series.type="pie".labels.distance `Number`*(default: 35)*

 The distance of the labels.

### series.type="pie".labels.font `String`*(default: "12px Arial, sans-serif")*

The font style of the labels.

### series.type="pie".labels.format `String`

The format of the labels.

#### Example

    //sets format of the labels
    format: "C"

### series.type="pie".labels.margin `Number|Object`*(default: 0.5)*

 The margin of the labels.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and left margin to 1px
    // margin right and bottom are with 2px (by default)
    margin: { top: 1, left: 1 }

### series.type="pie".labels.padding `Number|Object`*(default: 0)*

 The padding of the labels.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // padding right and bottom are with 2px (by default)
    padding: { top: 1, left: 1 }

### series.type="pie".labels.position `String`*(default: "outsideEnd")*

Defines the position of the pie labels.


#### *"center"*

The labels are positioned at the center of the pie segments.

#### *"insideEnd"*

The labels are positioned inside, near the end of the pie segments.

#### *"outsideEnd"*

The labels are positioned outside, near the end of the pie segments.
             The labels and the pie segments are connected with connector line.

### series.type="pie".labels.template `String/Function`

The label template.
Template variables:


*   **value** - the point value
*   **percentage** - the point value represented as a percentage value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "pie",
                 name: "Series 1",
                 data: [
                     { value: 200, category: 2000 },
                     { value: 450, category: 2001 },
                     { value: 300, category: 2002 },
                     { value: 125, category: 2003 }
                 ],
                 labels: {
                     // label template
                     template: "#= value #%",
                     visible: true
                 }
             }
         ]
    });

### series.type="pie".labels.visible `Boolean`*(default: false)*

 The visibility of the labels.

### series.type="pie".opacity `Number`*(default: 1)*

 The series opacity.

### series.type="pie".overlay `Object`

The effects overlay.

### series.type="pie".overlay.gradient `String`*(default: "roundedBevel")*

 The gradient name.
Available options are "none", "sharpBevel" and "roundedBevel".

### series.type="pie".padding `Number`

The padding around the pie chart (equal on all sides).

### series.type="pie".startAngle `number`*(default: 90)*

 The start angle of the first pie segment.

### series.type="pie".tooltip `Object`

The data point tooltip configuration options.

### series.type="pie".tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### series.type="pie".tooltip.border `Object`

The border configuration options.

### series.type="pie".tooltip.border.color `String`*(default: "black")*

 The color of the border.

### series.type="pie".tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="pie".tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### series.type="pie".tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### series.type="pie".tooltip.format `String`

The tooltip format.

#### Example

    //sets format of the tooltip
    format: "C"

### series.type="pie".tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### series.type="pie".tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value** - the point value
*   **percentage** - the point value represented as a percentage value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "pie",
                 name: "Series 1",
                 data: [200, 450, 300, 125],
                 tooltip: {
                     visible: true,
                     template: "#= category # - #= value #"
                 }
             }
         ]
    });

### series.type="pie".tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### series.type="pie".visibleInLegendField `Number`

A boolean value indicating whether to show the sector in the legend.

### series.type="pie".visibleInLegendField `Number`

A boolean value indicating whether to show the sector in the legend.

### series.type="scatter"

Available options for scatter series:

### series.type="scatter".color `String`

The series base color.

### series.type="scatter".data `Array`

Array of data items (optional).
The scatter chart can be bound to an array of arrays with two numbers (X and Y).


#### Example

    // ...
     series:[{
         type: "scatter",
         data:[[1, 1], [1, 2]],
         name: "Points"
     }]
     // ...

### series.type="scatter".labels `Object`

Configures the series data labels.

### series.type="scatter".labels.background `String`

The background color of the labels.

### series.type="scatter".labels.border `Object`

The border of the labels.

### series.type="scatter".labels.border.color `String`*(default: "black")*

 The color of the border.

### series.type="scatter".labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="scatter".labels.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="scatter".labels.color `String`

The text color of the labels.

### series.type="scatter".labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.

### series.type="scatter".labels.format `String`

The format of the labels.

#### Example

    //sets format of the labels
    format: "C"

### series.type="scatter".labels.margin `Number|Object`*(default: { left: 5, right: 5})*

The margin of the labels.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and bottom margin to 1px
    // margin left and right are with 5px (by default)
    margin: { top: 1, bottom: 1 }

### series.type="scatter".labels.padding `Number|Object`*(default: 0)*

 The padding of the labels.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // padding right and bottom are with 0px (by default)
    padding: { top: 1, left: 1 }

### series.type="scatter".labels.position `String`*(default: "above")*

Defines the position of the scatter labels.


#### *"above"*

The label is positioned at the top of the scatter chart marker.

#### *"right"*

The label is positioned at the right of the scatter chart marker.

#### *"below"*

The label is positioned at the bottom of the scatter chart marker.

#### *"left"*

The label is positioned at the left of the scatter chart marker.

### series.type="scatter".labels.template `String/Function`

The label template.
Template variables:


*   **value.x** - the x value
*   **value.y** - the y value
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "scatter",
                 name: "Series 1",
                 data: [[1, 1], [1, 2], [1, 3]],
                 labels: {
                     // label template
                     template: "#= value.x # - #= value.y x #",
                     visible: true
                 }
             }
         ]
    });

### series.type="scatter".labels.visible `Boolean`*(default: false)*

 The visibility of the labels.

### series.type="scatter".markers `Object`

Configures the scatter markers.

### series.type="scatter".markers.background `String`

The background color of the current series markers.

### series.type="scatter".markers.border `Object`

The border of the markers.

### series.type="scatter".markers.border.color `String`*(default: "black")*

 The color of the border.

### series.type="scatter".markers.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="scatter".markers.size `Number`*(default: 6)*

 The marker size.

### series.type="scatter".markers.type `String`*(default: "circle")*

Configures the markers shape type.


#### *"square"*

The marker shape is square.

#### *"triangle"*

The marker shape is triangle.

#### *"circle"*

The marker shape is circle.

### series.type="scatter".markers.visible `Boolean`*(default: true)*

 The markers visibility.

### series.type="scatter".name `String`

The series name.

### series.type="scatter".opacity `Number`*(default: 1)*

 The series opacity.

### series.type="scatter".tooltip `Object`

The data point tooltip configuration options.

### series.type="scatter".tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### series.type="scatter".tooltip.border `Object`

The border configuration options.

### series.type="scatter".tooltip.border.color `String`*(default: "black")*

 The color of the border.

### series.type="scatter".tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="scatter".tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### series.type="scatter".tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### series.type="scatter".tooltip.format `String`

The tooltip format.

#### Example

    //sets format of the tooltip
    format: "{0:C}--{1:C}"

### series.type="scatter".tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### series.type="scatter".tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value.x** - the x value
*   **value.y** - the y value
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "scatter",
                 name: "Series 1",
                 data: [[1, 1], [1, 2], [1, 3]],
                 tooltip: {
                     visible: true,
                     template: "#= category # - #= value.x # - #= value.y #"
                 }
             }
         ]
    });

### series.type="scatter".tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### series.type="scatter".xAxis `String`*(default: primary)*

 The name of the X axis to use.

### series.type="scatter".yAxis `String`*(default: primary)*

 The name of the Y axis to use.

### series.type="scatterLine"

Available options for scatter line series:

### series.type="scatterLine".color `String`

The series base color.

### series.type="scatterLine".dashType `String`*(default: "solid")*

 The dash type of the line.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="scatterLine".data `Array`

Array of data items (optional).
The scatter chart can be bound to an array of arrays with two numbers (X and Y).


#### Example

    // ...
     series:[{
         type: "scatterLine",
         data:[[1, 1], [1, 2]],
         name: "Points"
     }]
     // ...

### series.type="scatterLine".labels `Object`

Configures the series data labels.

### series.type="scatterLine".labels.background `String`

The background color of the labels.

### series.type="scatterLine".labels.border `Object`

The border of the labels.

### series.type="scatterLine".labels.border.color `String`*(default: "black")*

 The color of the border.

### series.type="scatterLine".labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### series.type="scatterLine".labels.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="scatterLine".labels.color `String`

The text color of the labels.

### series.type="scatterLine".labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.

### series.type="scatterLine".labels.format `String`

The format of the labels.

#### Example

    //sets format of the labels
    format: "{0:C}--{1:C}"

### series.type="scatterLine".labels.margin `Number|Object`*(default: { left: 5, right: 5})*

The margin of the labels.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3

    // sets the top and bottom margin to 1px
    // margin left and right are with 5px (by default)
    margin: { top: 1, bottom: 1 }

### series.type="scatterLine".labels.padding `Number|Object`*(default: 0)*

 The padding of the labels.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // padding right and bottom are with 0px (by default)
    padding: { top: 1, left: 1 }

### series.type="scatterLine".labels.position `String`*(default: "above")*

Defines the position of the scatter labels.


#### *"above"*

The label is positioned at the top of the scatter chart marker.

#### *"right"*

The label is positioned at the right of the scatter chart marker.

#### *"below"*

The label is positioned at the bottom of the scatter chart marker.

#### *"left"*

The label is positioned at the left of the scatter chart marker.

### series.type="scatterLine".labels.template `String/Function`

The label template.
Template variables:


*   **value.x** - the x value
*   **value.y** - the y value
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "scatterLine",
                 name: "Series 1",
                 data: [[1, 1], [1, 2], [1, 3]],
                 labels: {
                     // label template
                     template: "#= value.x # - #= value.y #",
                     visible: true
                 }
             }
         ]
    });

### series.type="scatterLine".labels.visible `Boolean`*(default: false)*

 The visibility of the labels.

### series.type="scatterLine".markers `Object`

Configures the scatter markers.

### series.type="scatterLine".markers.background `String`

The background color of the current series markers.

### series.type="scatterLine".markers.border `Object`

The border of the markers.

### series.type="scatterLine".markers.border.color `String`*(default: "black")*

 The color of the border.

### series.type="scatterLine".markers.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="scatterLine".markers.size `Number`*(default: 6)*

 The marker size.

### series.type="scatterLine".markers.type `String`*(default: "circle")*

Configures the markers shape type.


#### *"square"*

The marker shape is square.

#### *"triangle"*

The marker shape is triangle.

#### *"circle"*

The marker shape is circle.

### series.type="scatterLine".markers.visible `Boolean`*(default: true)*

 The markers visibility.

### series.type="scatterLine".missingValues `String`*(default: "gap")*

Configures the behavior for handling missing values in scatter series.


#### *"interpolate"*

The value is interpolated from neighboring points.

#### *"zero"*

The value is assumed to be zero.

#### *"gap"*

The line stops before the missing point and continues after it.

### series.type="scatterLine".name `String`

The series name.

### series.type="scatterLine".opacity `Number`*(default: 1)*

 The series opacity.

### series.type="scatterLine".tooltip `Object`

The data point tooltip configuration options.

### series.type="scatterLine".tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### series.type="scatterLine".tooltip.border `Object`

The border configuration options.

### series.type="scatterLine".tooltip.border.color `String`*(default: "black")*

 The color of the border.

### series.type="scatterLine".tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### series.type="scatterLine".tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### series.type="scatterLine".tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### series.type="scatterLine".tooltip.format `String`

The tooltip format.

#### Example

    //sets format of the tooltip
    format: "C"

### series.type="scatterLine".tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### series.type="scatterLine".tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value.x** - the x value
*   **value.y** - the y value
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 type: "scatterLine",
                 name: "Series 1",
                 data: [[1, 1], [1, 2], [1, 3]],
                 tooltip: {
                     visible: true,
                     template: "#= category # - #= value.x # - #= value.y #"
                 }
             }
         ]
    });

### series.type="scatterLine".tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### series.type="scatterLine".width `Number`*(default: 1)*

 The line width of the scatter line chart.

### series.type="scatterLine".xAxis `String`*(default: primary)*

 The name of the X axis to use.

### series.type="scatterLine".yAxis `String`*(default: primary)*

 The name of the Y axis to use.

### series.type="verticalArea"

Vertical area series use the same options as area series.
The category axis is rendered vertically instead of horizontally.

### series.type="verticalLine"

Vertical line series accepts the same parameters as line series.
The line and the category axis are now vertical instead of horizontal.

### series.visibleInLegend `Boolean`*(default: true)*

 A value indicating whether to show the series in the legend.

### seriesColors `Array`

The default colors for the chart's series. When all colors are used, new colors are pulled from the start again.

### seriesDefaults `Object`

Default values for each series.

### seriesDefaults.area `Object`

The area configuration options.
The default options for all area series. For more details see the series options.

### seriesDefaults.bar `Object`

The default options for all bar series. For more details see the series options.

### seriesDefaults.border `Object`

The border of the series.

### seriesDefaults.border.color `String`*(default: "black")*

 The color of the border.

### seriesDefaults.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### seriesDefaults.border.width `Number`*(default: 0)*

 The width of the border.

### seriesDefaults.bubble `Object`

The bubble configuration options.
The default options for all bubble series. For more details see the series options.

### seriesDefaults.column `Object`

The column configuration options.
The default options for all column series. For more details see the series options.

### seriesDefaults.donut `Object`

The donut configuration options.
The default options for all donut series. For more details see the series options.

### seriesDefaults.gap `Number`*(default: 1.5)*

 The distance between category clusters.

### seriesDefaults.labels `Object`

Configures the series data labels.

#### Example

    $("#chart").kendoChart({
        seriesDefault: {
            // adjust the default label appearence for all series
            labels: {
                // set the margin on all sides to 1
                margin: 1,
                // format the labels as currency
                format: "C"
            }
        },
        ...
    });

### seriesDefaults.labels.background `String`

The background color of the labels. Any valid CSS color string will work here,
including hex and rgb.

### seriesDefaults.labels.border `Object`

The border of the labels.

### seriesDefaults.labels.border.color `String`*(default: "black")*

 The color of the border.

### seriesDefaults.labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### seriesDefaults.labels.border.width `Number`*(default: 0)*

 The width of the border.

### seriesDefaults.labels.color `String`

The text color of the labels. Any valid CSS color string will work here, inlcuding hex
and rgb.

### seriesDefaults.labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.
labels

#### Example

    $("#chart").kendoChart({
        seriesDefault: {
            // adjust the default label appearence for all series
            labels: {
                // set the font size to 14px
                font: "14px Arial,Helvetica,sans-serif"
            }
        },
        ...
    });

### seriesDefaults.labels.format `String`

The format of the labels.

#### Example

    //sets format of the labels
    format: "C"

### seriesDefaults.labels.margin `Number|Object`*(default: 0)*

 The margin of the labels.

#### Example

    $("#chart).kendoChart({
         labels: {
             // sets the top, right, bottom and left margin to 3px.
             margin: 3
         },
         ...
    });
    //
    $("#chart").kendoChart({
         labels: {
             // sets the top and left margin to 1px
             // margin right and bottom are with 0px (by default)
             margin: { top: 1, left: 1 }
         },
         ...
    });

### seriesDefaults.labels.padding `Number|Object`*(default: 0)*

 The padding of the labels.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // padding right and bottom are with 0px (by default)
    padding: { top: 1, left: 1 }

### seriesDefaults.labels.template `String/Function`

The label template.
Template variables:


*   **value** - the point value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         seriesDefault: {
             labels: {
                 // label template
                 template: "#= value  #%",
                 visible: true
             }
         },
         series: [
             {
                 name: "Series 1",
                 data: [200, 450, 300, 125]
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         }
    });

### seriesDefaults.labels.visible `Boolean`*(default: false)*

 The visibility of the labels.

#### Example

    $("#chart").kendoChart({
        seriesDefault: {
            labels: {
                // hide all the series labels by default
                visible: true
            },
            ...
        }
    });

### seriesDefaults.line `Object`

The line configuration options.
The default options for all line series. For more details see the series options.

### seriesDefaults.overlay `Object`

The effects overlay.

### seriesDefaults.pie `Object`

The pie configuration options.
The default options for all pie series. For more details see the series options.

### seriesDefaults.scatter `Object`

The scatter configuration options.
The default options for all scatter series. For more details see the series options.

### seriesDefaults.scatterLine `Object`

The scatterLine configuration options.
The default options for all scatterLine series. For more details see the series options.

### seriesDefaults.spacing `Number`*(default: 0.4)*

 Space between bars.

### seriesDefaults.stack `Boolean`*(default: false)*

A value indicating if the series should be stacked.

### seriesDefaults.tooltip `Object`

The data point tooltip configuration options.

### seriesDefaults.tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### seriesDefaults.tooltip.border `Object`

The border configuration options.

### seriesDefaults.tooltip.border.color `String`*(default: "black")*

 The color of the border.

### seriesDefaults.tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### seriesDefaults.tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### seriesDefaults.tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### seriesDefaults.tooltip.format `String`

The tooltip format.

#### Example

    //sets format of the tooltip
    format: "C"

### seriesDefaults.tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### seriesDefaults.tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value** - the point value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         seriesDefaults: {
             tooltip: {
                 visible: true,
                 template: "#= category # - #= value #"
             }
         },
         series: [
             {
                 name: "Series 1",
                 data: [200, 450, 300, 125]
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         }
    });

### seriesDefaults.tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### seriesDefaults.verticalArea `Object`

The vertical area configuration options.
The default options for all vertical area series. For more details see the series options.

### seriesDefaults.verticalLine `Object`

The vertical line configuration options.
The default options for all vertical line series. For more details see the series options.

### theme `String`

Sets Chart theme. Available themes: default, blueOpal, black.

### title `Object`

The chart title configuration options.

### title.align `String`*(default: "center")*

 The alignment of the title.


#### *"left"*

The text is aligned to the left.

#### *"center"*

The text is aligned to the middle.

#### *"right"*

The text is aligned to the right.

### title.background `String`*(default: "white")*

 The background color of the title.

### title.border `Object`

The border of the title.

#### Example

    $("#chart").kendoChart({
        // set border options on the title
        title: {
            border: {
                // set the border color to a dark blue
                color: "#336699",
                // set the width of the border to 2 pixels
                width: 2,
                // set the border style to long dashes
                dashType: "longDash"
            }
        },
        ...
    });

### title.border.color `String`*(default: "black")*

 The color of the border.

### title.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### title.border.width `Number`*(default: 0)*

 The width of the border.

### title.font `String`*(default: "16px Arial,Helvetica,sans-serif")*

 The font of the title.

### title.margin `Number | Object`*(default: 5)*

 The margin of the title.

#### Example

    $("#chart").kendoChart({
        // sets the top, right, bottom and left margin to 3px.
        title: {
            margin: 3
        },
        ...
    });
    //
    $("#chart").kendoChart({
        // sets the top and left margin to 1px
        // margin right and bottom are with 5px (by default)
        title: {
            margin: { top: 1, left: 1 }
        },
        ...
    });

### title.padding `Number | Object`*(default: 5)*

 The padding of the title.

#### Example

    $("#chart").kendoChart({
        // sets the top, right, bottom and left padding to 3px.
        title: {
            padding: 3
        },
        ...
    });
    //
    $("#chart").kendoChart({
        // sets the top and left padding to 1px
        // padding right and bottom are with 5px (by default)
        title: {
            padding: { top: 1, left: 1 }
        },
        ...
    });

### title.position `String`*(default: "top")*

 The position of the title.


#### *"top"*

The title is positioned on the top.

#### *"bottom"*

The title is positioned on the bottom.

### title.text `String`

The title of the chart.

### title.visible `Boolean`*(default: false)*

 The visibility of the title.

#### Example

    $("#chart ").kendoChart({
        title: {
            // hides the title
            visible: false
        },
        ...
    });

### tooltip `Object`

The data point tooltip configuration options.

### tooltip.background `String`

The background color of the tooltip. The default is determined from the series color.

### tooltip.border `Object`

The border configuration options.

### tooltip.border.color `String`*(default: "black")*

 The color of the border.

### tooltip.border.width `Number`*(default: 0)*

 The width of the border.

### tooltip.color `String`

The text color of the tooltip. The default is the same as the series labels color.

### tooltip.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

 The tooltip font.

### tooltip.format `String`

The tooltip format.

#### Example

    //sets format of the tooltip
    format: "C"

### tooltip.padding `Number|Object`

The padding of the tooltip.

#### Example

    // sets the top, right, bottom and left padding to 3px.
    padding: 3

    // sets the top and left padding to 1px
    // right and bottom padding are left at their default values
    padding: { top: 1, left: 1 }

### tooltip.template `String|Function`

The tooltip template.
Template variables:


*   **value** - the point value
*   **category** - the category name
*   **series** - the data series
*   **dataItem** - the original data item used to construct the point.
        Will be null if binding to array.

#### Example

    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 name: "Series 1",
                 data: [200, 450, 300, 125]
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         },
         tooltip: {
             visible: true,
             template: "#= category # - #= value #"
         }
    });

### tooltip.visible `Boolean`*(default: false)*

 A value indicating if the tooltip should be displayed.

### transitions `Boolean`*(default: true)*

A value indicating if transition animations should be played.

### valueAxis `Object`

The value axis configuration options.

### valueAxis.axisCrossingValue `Number`*(default: 0)*

 Value at which the category axis crosses this axis.

### valueAxis.color `String`

Color to apply to all axis elements.
Individual color settings for line and labels take priority. Any valid CSS color string will work here, including hex and rgb.

### valueAxis.labels `Object`

Configures the axis labels.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            labels: {
                // set the color of the text on the labels to a dark blue
                color: "#336699",
                // set the background color of the labels to a light grey
                background: "#e2e2e2",
                // make the font 14px
                // rotate the labels just slightly for visual effect
                rotation: 10,
                // format the labels for currency
                format: "C"
            }
        },
        ...
    });

### valueAxis.labels.background `String`

The background color of the labels. Any valid CSS color string will work here, including
hex and rgb

### valueAxis.labels.border `Object`

The border of the labels.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            labels: {
                border: {
                    // make the width 1
                    width: 1,
                    // set the color to a dark blue
                    color: "#336699",
                    // set the border style to dashed
                    dashType: "dash"
                }
            }
        },
        ...
    });

### valueAxis.labels.border.color `String`*(default: "black")*

 The color of the border. Any valid CSS color string will work here, including
hex and rgb.

### valueAxis.labels.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### valueAxis.labels.border.width `Number`*(default: 0)*

 The width of the border.

### valueAxis.labels.color `String`

The text color of the labels. Any valid CSS color string will work here, including hex and rgb.

### valueAxis.labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.

### valueAxis.labels.format `String`

The format of the labels.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
           labels: {
               // set the format to currency
               format: "C"
           }
        },
        ...
    });

### valueAxis.labels.margin `Number|Object`*(default: 0)*

 The margin of the labels.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            label: {
                // sets the top, right, bottom and left margin to 3px.
                margin: 3
           }
        },
        ...
    });
    //
    $("#chart").kendoChart({
        valueAxis: {
            label: {
                // sets the top and left margin to 1px
                // margin right and bottom are with 0px (by default)
                margin: { top: 1, left: 1 }
            }
        },
        ...
    });

### valueAxis.labels.mirror `Boolean`

Mirrors the axis labels and ticks.
If the labels are normally on the left side of the axis,
mirroring the axis will render them to the right.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            labels: {
                // mirror the labels on the right
                 mirror: true
            }
        },
        ...
    });

### valueAxis.labels.padding `Number | Object`*(default: 0)*

 The padding of the labels.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            label: {
                // sets the top, right, bottom and left padding to 3px.
                padding: 3
            }
        },
        ...
    });
    //
    $("#chart").kendoChart({
        valueAxis: {
            label: {
                // sets the top and left padding to 1px
                // padding right and bottom are with 0px (by default)
                padding: { top: 1, left: 1 }
            }
        },
        ...
    });

### valueAxis.labels.rotation `Number`*(default: 0)*

 The rotation angle of the labels.

### valueAxis.labels.skip `Number`*(default: 1)*

 Number of labels to skip.
Skips rendering the first n labels.

### valueAxis.labels.step `Number`*(default: 1)*

 Label rendering step.
Every n-th label is rendered where n is the step

### valueAxis.labels.template `String/Function`

The label template.
Template variables:


*   **value** - the value

#### Example

    // chart intialization
    $("#chart").kendoChart({
         title: {
             text: "My Chart Title"
         },
         series: [
             {
                 name: "Series 1",
                 data: [200, 450, 300, 125]
             }
         ],
         categoryAxis: {
             categories: [2000, 2001, 2002, 2003]
         },
         valueAxis: {
             labels: {
                 // labels template
                 template: "#= value #%"
             }
         }
    });

### valueAxis.labels.visible `Boolean`*(default: true)*

 The visibility of the labels.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            labels: {
                // hide the axis labels
                visible: false
            }
       },
       ...
    });

### valueAxis.line `Object`

Configures the axis line. This will also affect the major and minor ticks, but not the grid lines.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            line: {
                // change the line width to 2 pixels
                width: 2,
                // set the color to light grey
                color: "#e2e2e2"
            }
        },
        ...
    });

### valueAxis.line.color `String`*(default: "black")*

 The color of the line. This will also effect the major and minor ticks, but
not the grid lines.

### valueAxis.line.dashType `String`*(default: "solid")*

 The dash type of the line.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### valueAxis.line.visible `Boolean`*(default: true)*

 The visibility of the line.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            line: {
                // hide the axis lines altogether
                visible: false
            }
        },
        ...
    });

### valueAxis.line.width `Number`*(default: 1)*

 The width of the line. This will also effect the major and minor ticks, but
not the grid lines.

### valueAxis.majorGridLines `Object`

Configures the major grid lines.  These are the lines that are an extension of the major ticks through the
body of the chart.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            minorGridLines: {
                // set visible to true
                visible: true,
                // set width to 2 pixels
                width: 2,
                // set the color to a dark blue
                color: "#336699",
                // set the dashType to dot
                dashType: "dot"
            }
        },
        ...
    });

### valueAxis.majorGridLines.color `String`*(default: "black")*

 The color of the lines.

### valueAxis.majorGridLines.visible `Boolean`*(default: true)*

 The visibility of the lines.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            minorGridLines: {
                // set visible to true
                visible: false
            }
        },
        ...
    });

### valueAxis.majorGridLines.width `Number`*(default: 1)*

 The width of the lines.

### valueAxis.majorTicks `Object`

The major ticks of the axis.

### valueAxis.majorTicks.size `Number`*(default: 4)*

 The axis major tick size. This is the length of the line in pixels that is drawn to indicate the tick
on the chart.

### valueAxis.majorTicks.visible `Boolean`*(default: true)*

 The visibility of the major ticks.

### valueAxis.majorUnit `Number`

The interval between major divisions.

### valueAxis.max `Number`*(default: 1)*

 The maximum value of the axis.
This is often used in combination with the **min** configuration option.

### valueAxis.min `Number`*(default: 0)*

 The minimum value of the axis.
This is often used in combination with the **max** configuration option.

### valueAxis.minorGridLines `Object`

Configures the minor grid lines.  These are the lines that are an extension of the minor ticks through the

### valueAxis.minorGridLines.color `String`*(default: "black")*

 The color of the lines.


Note that this has no effect if the visibility of the minor grid lines is not set to **true**.

### valueAxis.minorGridLines.dashType `String`*(default: "solid")*

 The dash type of the minor grid lines.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.
body of the chart.

Note that minor grid lines are not visible by default, therefore none of these settings will take effect without the minor grid
lines visibility being set to **true**
.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            minorGridLines: {
                // set visible to true
                visible: true,
                // set width to 2 pixels
                width: 2,
                // set the color to a dark blue
                color: "#336699",
                // set the dashType to dot
                dashType: "dot"
            }
        },
        ...
    });

### valueAxis.minorGridLines.visible `Boolean`*(default: false)*

 The visibility of the lines.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            minorGridLines: {
                // set visible to true. they are hidden by default
                visible: true
            }
        },
        ...
    });

### valueAxis.minorGridLines.width `Number`*(default: 1)*

 The width of the lines.


Note that this settings has no effect if the visibility of the minor grid lines is not set to **true**.

### valueAxis.minorTicks `Object`

The minor ticks of the axis.

### valueAxis.minorTicks.size `Number`*(default: 3)*

 The axis minor tick size. This is the length of the line in pixels that is drawn to indicate the tick
on the chart.

### valueAxis.minorTicks.visible `Boolean`*(default: false)*

 The visibility of the minor ticks.

### valueAxis.minorUnit `Number`

The interval between minor divisions.
It defaults to 1/5th of the majorUnit.

### valueAxis.name `Object`*(default: primary)*

 The unique axis name.

### valueAxis.plotBands `Array`

The plot bands of the value axis.
The plot band fields:


#### *"from"*

The start position of the plot band in axis units.

#### *"to"*

The end position of the plot band in axis units.

#### *"color"*

The color of the plot band.

#### Example

    $("#chart").kendoChart({
        ...,
        valueAxis: {
            plotBands: [{
                from: 0.2,
                to: 0.4,
                color: "green"
            }]
        },
     });

### valueAxis.reverse `Boolean`*(default: false)*

 Reverses the axis direction -
values increase from right to left and from top to bottom.

### valueAxis.title `Object`

The title of the value axis.

#### Example

    $("#chart").kendoChart({
        title: {
            // set the color of the title text to a dark blue
            color: "#336699",
            // set the background color to a light grey
            background: "#e2e2e2",
            // set the text of the title
            text: "Sales By District",
            // move the title to the bottom
            position: "bottom"
        },
        ...
    });

### valueAxis.title.background `String`

The background color of the title. Any valid CSS color string will work here, including
hex and rgb.

### valueAxis.title.border `Object`

The border of the title.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            title: {
                // tweak the border around the title
                border: {
                    // set the width to 1
                    width: 1,
                    // set the color to a dark blue
                    color: "#336699",
                    // set the style to dashed
                    dashType: "dash"
                }
            }
        },
        ...
    });

### valueAxis.title.border.color `String`*(default: "black")*

 The color of the border.

### valueAxis.title.border.dashType `String`*(default: "solid")*

 The dash type of the border.


#### *"solid"*

Specifies a solid line.

#### *"dot"*

Specifies a line consisting of dots.

#### *"dash"*

Specifies a line consisting of dashes.

#### *"longDash"*

Specifies a line consisting of a repeating pattern of long-dash.

#### *"dashDot"*

Specifies a line consisting of a repeating pattern of dash-dot.

#### *"longDashDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot.

#### *"longDashDotDot"*

Specifies a line consisting of a repeating pattern of long-dash-dot-dot.

### valueAxis.title.border.width `Number`*(default: 0)*

 The width of the border.

### valueAxis.title.color `String`

The text color of the title. Any valid CSS color string will work here, including hex and rgb.

### valueAxis.title.font `String`*(default: "16px Arial,Helvetica,sans-serif")*

The font style of the title.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            title: {
                // decreate the font size of the title to 14 px
                font: "14px Arial,Helvetica,sans-serif"
            }
        }
        ...
    });

### valueAxis.title.margin `Number | Object`*(default: 5)*

 The margin of the title.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            title: {
                // sets the top, right, bottom and left margin to 3px.
                margin: 3
            }
        },
        ...
    });
    //
    $("#chart").kendoChart({
        valueAxis: {
            title: {
                // sets the top and left margin to 1px
                // margin right and bottom are with 0px (by default)
                margin: { top: 1, left: 1 }
            }
        },
        ...
    });

### valueAxis.title.padding `Number | Object`*(default: 0)*

 The padding of the title.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            title: {
                // sets the top, right, bottom and left padding to 3px.
                padding: 3
            }
        },
        ...
    });
    $("#chart").kendoChart({
        valueAxis: {
            title: {
                // sets the top and left padding to 1px
                // padding right and bottom are with 0px (by default)
                padding: { top: 1, left: 1 }
            }
        },
        ...
    });

### valueAxis.title.position `String`*(default: "center")*

 The position of the title.


#### *"top"*

The axis title is positioned on the top (applicable to vertical axis).

#### *"bottom"*

The axis title is positioned on the bottom (applicable to vertical axis).

#### *"left"*

The axis title is positioned on the left (applicable to horizontal axis).

#### *"right"*

"The axis title is positioned on the right (applicable to horizontal axis).

#### *"center"*

"The axis title is positioned in the center.

### valueAxis.title.rotation `Number`*(default: 0)*

 The rotation angle of the title.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            title: {
                // rotate the title 20 degrees
                rotate: 20
            }
        },
        ...
    });

### valueAxis.title.text `String`

The text of the title.

### valueAxis.title.visible `Boolean`*(default: true)*

 The visibility of the title.

#### Example

    $("#chart").kendoChart({
        valueAxis: {
            title: {
                // hide the title
                visible: false
            }
        },
        ...
    });

### valueAxis.visible `Boolean`*(default: true)*

 The visibility of the axis.

### xAxis `Object`

Scatter charts X-axis configuration options.
Includes **all valueAxis options** in addition to:

### xAxis.type `String`*(default: "Numeric")*

 The axis type.


Note: The Chart will automatically switch to a date axis if the series X value
is of type Date. Specify type explicitly when such behavior is undesired.



#### *"Numeric"*

Generic axis with automatic range.

#### *"Date"*

Suitable for displaying chronological data.

### xAxis.type: "Date"

Properties specific to the date-time value axis

### xAxis.type: "Date".axisCrossingValue `Date`

Date at which the Y axis crosses this axis.

### xAxis.type: "Date".baseUnit `String`

The base time interval for the axis labels.
The default baseUnit is determined automatically from the value range. Available options:

* minutes
* hours
* days
* months
* years

### xAxis.type: "Date".labels `Object`

Label settings specific to the date axis.

### xAxis.type: "Date".labels.culture `String`*(default: global culture)*

Culture to use for formatting the dates. See [Globalization](http://www.kendoui.com/documentation/framework/globalization/overview.aspx) for more information.

### xAxis.type: "Date".labels.dateFormats `Object`

Date format strings


#### *"hours"*

"HH:mm"

#### *"days"*

"M/d"

#### *"months"*

"MMM 'yy"

#### *"years"*

"yyyy"
The Chart will choose the appropriate format for the current `baseUnit`.
Setting the labels **format** option will override these defaults.

### xAxis.type: "Date".majorUnit `Number`

The interval between major divisions in base units.

### xAxis.type: "Date".max `Date`

The end date of the axis.
This is often used in combination with the **min** configuration option.

### xAxis.type: "Date".min `Date`

The start date of the axis.
This is often used in combination with the **max** configuration option.

### xAxis.type: "Date".minorUnit `Number`

The interval between minor divisions in base units.
It defaults to 1/5th of the majorUnit.

### xAxis.type: "Numeric" `Number`

Options specific to the numeric axis.

### xAxis.type: "Numeric".axisCrossingValue *(default: 0)*

Value at which the first Y axis crosses this axis.

### xAxis.type: "Numeric".axisCrossingValue `Array`*(default: [0])*

Values at which the Y axes cross this X axis.
<p>
**Note:&nbsp;** Specify a value greater than or equal to the
axis maximum value to denote the far end of the axis.

#### Example

    $("#chart").kendoChart({
         ...,
         xAxis: {
             axisCrossingValue: [0, 1000]
         },
         yAxis: [{ }, { name: "secondary" }],
         ...
    });
    </p>

### yAxis `Object`

The scatter charts Y-axis configuration options.
See **xAxis** for list of available options.

## Methods

### destroy

Prepares the Chart for safe removal from the DOM.

Detaches event handlers and removes data entries in order to avoid memory leaks.

#### Example

	// deatach events
    $("#chart").data("kendoChart").destroy();

	// remove chart html from DOM
    $("#chart").remove();

### refresh

Reloads the data and repaints the chart.

#### Example

    var chart = $("#chart").data("kendoChart");

    // refreshes the chart
    chart.refresh();

### svg

Returns the SVG representation of the current chart.
The returned string is a self-contained SVG document
that can be used as is or converted to other formats
using tools like [Inkscape](http://inkscape.org/) and
[ImageMagick](http://www.imagemagick.org/).
Both programs provide command-line interface
suitable for backend processing.

#### Example

    var chart = $("#chart").data("kendoChart");
    var svgText = chart.svg();

## Events

### axisLabelClick

Fires when an axis label is clicked.

#### Example

    function onAxisLabelClick(e) {
        alert("Clicked " + e.axis.type + " axis label with value: " + e.value);
    }

#### Event Data

##### e.axis `Object`

The axis that the label belongs to.

##### e.value `Object`

The label value or category name.

##### e.text `Object`

The label text.

##### e.index `Object`

The label sequential index or category index.

##### e.dataItem `Object`

The original data item used to generate the label.
Applicable only for data bound category axis.

##### e.element `Object`

The DOM element of the label.

### dataBound

Fires when the chart has received data from the data source
and is about to render it.

#### Example

    function onDataBound(e) {
        // Series data is now available
    }

### plotAreaClick

Fires when plot area is clicked.

#### Example

    function onPlotAreaClick(e) {
        alert("Clicked X axis value: " + e.x);
    }

#### Event Data

##### e.value `Object`

The data point value.
Available only for categorical charts (bar, line, area and similar).

##### e.category `Object`

The data point category.
Available only for categorical charts (bar, line, area and similar).

##### e.element `Object`

The DOM element of the plot area.

##### e.x `Object`

The X axis value or array of values for multi-axis charts.

##### e.y `Object`

The X axis value or array of values for multi-axis charts.

### seriesClick

Fires when chart series are clicked.

#### Example

    function onSeriesClick(e) {
        alert("Clicked value: " + e.value);
    }

#### Event Data

##### e.value `Object`

The data point value.

##### e.category `Object`

The data point category

##### e.series `Object`

The clicked series.

##### e.series.type `String`

The series type

##### e.series.name `String`

The series name

##### e.series.data `Array`

The series data points

##### e.dataItem `Object`

The original data item (when binding to dataSource).

##### e.element `Object`

The DOM element of the data point.

### seriesHover

Fires when chart series are hovered.

#### Example

    function onSeriesHover(e) {
        alert("Hovered value: " + e.value);
    }

#### Event Data

##### e.value `Object`

The data point value.

##### e.category `Object`

The data point category

##### e.series `Object`

The clicked series.

##### e.series.type `String`

The series type

##### e.series.name `String`

The series name

##### e.series.data `Array`

The series data points

##### e.dataItem `Object`

The original data item (when binding to dataSource).

##### e.element `Object`

The DOM element of the data point.
