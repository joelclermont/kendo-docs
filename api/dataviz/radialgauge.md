---
title: kendo.dataviz.ui.RadialGauge
tags: api,dataviz
publish: true
---

# kendo.dataviz.ui.RadialGauge

## Description



The Radial Gauge widget is used to let users quickly understand where a value lies in a certain range.
All graphics are rendered on the client using SVG with a fallback to VML for legacy browsers.


### 
Getting Started

#### 1\. Create a simple HTML div (optionally set a height and width with CSS)

    <div id="radial-gauge"></div>

#### 2\. Initialize the Kendo UI RadialGauge with default configuration

       $(document).ready(function() {
           $("#radial-gauge").kendoRadialGauge();
       });
    </p>

### Creating half- and quarter-circle gauges

The `startAngle` and `endAngle` configuration options enable you to create
gauges that align with your design goals.

#### Create a quarter-gauge, oriented to the top-right

        $("#radial-gauge").kendoRadialGauge({
            startAngle: 90,
            endAngle: 180
        });

For a real-world example for this functionality, see the car dashboard demo.

## Configuration

### gaugeArea `Object`

The gauge area configuration options.
This is the entire visible area of the gauge.

### gaugeArea.background `Object`*(default: "white")*

 The background of the gauge area.
Any valid CSS color string will work here, including hex and rgb.

### gaugeArea.border `Object`

The border of the gauge area.

### gaugeArea.border.color `String`*(default: "black")*

The color of the border. Any valid CSS color string will work here, including hex and rgb.

### gaugeArea.border.dashType `String`*(default: "solid")*

The dash type of the border.
<div class="details-list">
    <dl>
        <dt>
             `"solid"`
        </dt>
        <dd>
             Specifies a solid line.
        </dd>
        <dt>
             `"dot"`
        </dt>
        <dd>
             Specifies a line consisting of dots.
        </dd>
        <dt>
             `"dash"`
        </dt>
        <dd>
             Specifies a line consisting of dashes.
        </dd>
        <dt>
             `"longDash"`
        </dt>
        <dd>
             Specifies a line consisting of a repeating pattern of long-dash.
        </dd>
        <dt>
             `"dashDot"`
        </dt>
        <dd>
             Specifies a line consisting of a repeating pattern of dash-dot.
        </dd>
        <dt>
             `"longDashDot"`
        </dt>
        <dd>
             Specifies a line consisting of a repeating pattern of long-dash-dot.
        </dd>
        <dt>
             `"longDashDotDot"`
        </dt>
        <dd>
             Specifies a line consisting of a repeating pattern of long-dash-dot-dot.
        </dd>
   </dl>
</div>

### gaugeArea.border.width `Number`*(default: 0)*

 The width of the border.

### gaugeArea.height `Number`*(default: vertical gauge is 200px; horizontal gauge is 60px)*

The height of the gauge area.

### gaugeArea.margin `Number|Object`*(default: 5)*

 The margin of the gauge area.

#### Example

    // sets the top, right, bottom and left margin to 3px.
    margin: 3
    
    // sets the top and left margin to 1px
    // margin right and bottom are with 5px (by default)
    margin: { top: 1, left: 1 }

### gaugeArea.width `Number`*(default: vertical gauge is 60px; horizontal gauge is 200px)*

The width of the gauge area.

### pointer `Object`

The pointer configuration options.

### pointer.cap `Object`

The cap configuration options.

### pointer.cap.color `String`

The color of the cap.
Any valid CSS color string will work here, including hex and rgb.

### pointer.cap.size `Number`

The size of the cap in percents. (from 0 to 1)

### pointer.color `String`

The color of the pointer.
Any valid CSS color string will work here, including hex and rgb.

### pointer.value `Number`

The value of the gauge.

### rangeSize `Number`

The width of the range indicators.

### scale `Object`

Configures the scale.

### scale.endAngle `number`*(default: 210)*

 The end angle of the gauge.
The gauge is rendered clockwise(0 degrees are the 180 degrees in the polar coordinat system)

### scale.labels `Object`

Configures the scale labels.

### scale.labels.background `String`

The background color of the labels.
Any valid CSS color string will work here, including hex and rgb

### scale.labels.border `Object`

The border of the labels.

### scale.labels.border.color `String`*(default: "black")*

The color of the border. Any valid CSS color string will work here, including hex and rgb.

### scale.labels.border.dashType `String`*(default: "solid")*

The dash type of the border.
<div class="details-list">
    <dl>
        <dt>
             `"solid"`
        </dt>
        <dd>
             Specifies a solid line.
        </dd>
        <dt>
             `"dot"`
        </dt>
        <dd>
             Specifies a line consisting of dots.
        </dd>
        <dt>
             `"dash"`
        </dt>
        <dd>
             Specifies a line consisting of dashes.
        </dd>
        <dt>
             `"longDash"`
        </dt>
        <dd>
             Specifies a line consisting of a repeating pattern of long-dash.
        </dd>
        <dt>
             `"dashDot"`
        </dt>
        <dd>
             Specifies a line consisting of a repeating pattern of dash-dot.
        </dd>
        <dt>
             `"longDashDot"`
        </dt>
        <dd>
             Specifies a line consisting of a repeating pattern of long-dash-dot.
        </dd>
        <dt>
             `"longDashDotDot"`
        </dt>
        <dd>
             Specifies a line consisting of a repeating pattern of long-dash-dot-dot.
        </dd>
   </dl>
</div>

### scale.labels.border.width `Number`*(default: 0)*

 The width of the border.

### scale.labels.color `String`

The text color of the labels.
Any valid CSS color string will work here, including hex and rgb.

### scale.labels.font `String`*(default: "12px Arial,Helvetica,sans-serif")*

The font style of the labels.

### scale.labels.format `String`

The format of the labels.

#### Example

    $("#radial-gauge").kendoRadialGauge({
        scale: {
           labels: {
               // set the format to currency
               format: "C"
           }
        }
    });

### scale.labels.margin `Number|Object`*(default: 0)*

 The margin of the labels.

### scale.labels.padding `Number | Object`*(default: 0)*

 The padding of the labels.

### scale.labels.position `String`*(default: "inside")*

The labels positions.
<div class="details-list">
    <dl>
        <dt>
             `"inside"`
        </dt>
        <dd>
             The labels are positioned inside.
        </dd>
        <dt>
             `"outside"`
        </dt>
        <dd>
             The labels are positioned outside.
        </dd>
   </dl>
</div>

### scale.labels.template `String/Function`

The label template.
Template variables:


*   **value** - the value

#### Example

    // chart intialization
    $("#radial-gauge").kendoRadialGauge({
         scale: {
             labels: {
                 // labels template
                 template: "#= value #%"
             }
         }
    });

### scale.labels.visible `Boolean`*(default: true)*

 The visibility of the labels.

### scale.majorTicks `Object`

Configures the scale major ticks.

### scale.majorTicks.color `String`

The color of the major ticks.

### scale.majorTicks.size `Number`

The major tick size.
This is the length of the line in pixels that is drawn to indicate the tick on the scale.

### scale.majorTicks.visible `Boolean`*(default: true)*

 The visibility of the major ticks.
Any valid CSS color string will work here, including hex and rgb.

### scale.majorTicks.width `Number`*(default: 0.5)*

 The width of the major ticks.

### scale.majorUnit `Number`

The interval between major divisions.

### scale.max `Number`*(default: 100)*

 The maximum value of the scale.

### scale.min `Number`*(default: 0)*

 The minimum value of the scale.

### scale.minorTicks `Object`

Configures the scale minor ticks.

### scale.minorTicks.color `String`

The color of the minor ticks.
Any valid CSS color string will work here, including hex and rgb.

### scale.minorTicks.size `Number`

The minor tick size.
This is the length of the line in pixels that is drawn to indicate the tick on the scale.

### scale.minorTicks.visible `Boolean`*(default: true)*

 The visibility of the minor ticks.

### scale.minorTicks.width `Number`*(default: 0.5)*

 The width of the minor ticks.

### scale.minorUnit `Number`

The interval between minor divisions.

### scale.ranges `Array`

The ranges of the scale.
The range fields:
<div class="details-list">
   <dl>
        <dt>
             `"from"`
        </dt>
        <dd>
             The start position of the range in scale units.
        </dd>
        <dt>
            `"to"`
        </dt>
        <dd>
             The end position of the range in scale units.
        </dd>
        <dt>
             `"color"`
        </dt>
        <dd>
             The color of the range.
Any valid CSS color string will work here, including hex and rgb.
        </dd>
   </dl>
</div>

#### Example

    $("#radial-gauge").kendoRadialGauge({
        scale: {
            ranges: [{
                from: 10,
                to: 20,
                color: "green"
            }]
        }
     });

### scale.reverse `Boolean`*(default: false)*

Reverses the scale direction - values are increase anticlockwise.

### scale.startAngle `number`*(default: -30)*

 The start angle of the gauge.
The gauge is rendered clockwise(0 degrees are the 180 degrees in the polar coordinat system)

### transitions `Boolean`*(default: true)*

A value indicating if transition animations should be played.

## Methods

### redraw

Redraws the gauge.

#### Example

    var gauge = $("#radial-gauge").data("kendoRadialGauge");
    gauge.redraw();

### svg

Returns the SVG representation of the current gauge.
The returned string is a self-contained SVG document
that can be used as is or converted to other formats
using tools like [Inkscape](http://inkscape.org/) and
[ImageMagick](http://www.imagemagick.org/).
Both programs provide command-line interface
suitable for backend processing.

#### Example

    var gauge = $("#radial-gauge").data("kendoRadialGauge");
    var svgText = gauge.svg();

### value

Change the value of the gauge.

#### Example

    var gauge = $("#radial-gauge").data("kendoRadialGauge");
    gauge.redraw();