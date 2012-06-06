## Description


kendo.dataviz.ui.LinearGauge.Description

The Linear Gauge widget is used to let users quickly understand where a value lies in a certain range.
All graphics are rendered on the client using SVG with a fallback to VML for legacy browsers.


### 
Getting Started

#### 1\. Create a simple HTML div (optionally set a height and width with CSS)

    <div id="linear-gauge"></div>


#### 2\. Initialize the Kendo UI Linear Gauge with default configuration

       $(document).ready(function() {
           $("#linear-gauge").kendoLinearGauge();
       });
    </p>


#### Create a horizontal linear gauge with value 20 and mininum value 10

        $("#linear-gauge").kendoLinearGauge({
            pointer: {
                value: 20
            },
            scale: {
                min: 10,
                vertical: false
            }
        });





------------------------------------------

## Configuration

### `gaugeArea` : **Object**  

The gauge area configuration options.This is the entire visible area of the gauge.

### `gaugeArea.background` : **Object** *(default: "white")* 

 The background of the gauge area.Any valid CSS color string will work here, including hex and rgb.

### `gaugeArea.border` : **Object**  

The border of the gauge area.

### `gaugeArea.border.color` : **String** *(default: "black")* 

The color of the border. Any valid CSS color string will work here, including hex and rgb.

### `gaugeArea.border.dashType` : **String** *(default: "solid")* 

The dash type of the border.<div class="details-list">    <dl>        <dt>             <code>"solid"</code>        </dt>        <dd>             Specifies a solid line.        </dd>        <dt>             <code>"dot"</code>        </dt>        <dd>             Specifies a line consisting of dots.        </dd>        <dt>             <code>"dash"</code>        </dt>        <dd>             Specifies a line consisting of dashes.        </dd>        <dt>             <code>"longDash"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash.        </dd>        <dt>             <code>"dashDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of dash-dot.        </dd>        <dt>             <code>"longDashDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash-dot.        </dd>        <dt>             <code>"longDashDotDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash-dot-dot.        </dd>   </dl></div>

### `gaugeArea.border.width` : **Number** *(default: 0)* 

 The width of the border.

### `gaugeArea.height` : **Number** *(default: vertical gauge is 200px; horizontal gauge is 60px)* 

The height of the gauge area.

### `gaugeArea.margin` : **Number|Object** *(default: 5)* 

 The margin of the gauge area.

#### Example



    // sets the top, right, bottom and left margin to 3px.
    margin: 3
    
    // sets the top and left margin to 1px
    // margin right and bottom are with 5px (by default)
    margin: { top: 1, left: 1 }

### `gaugeArea.width` : **Number** *(default: vertical gauge is 60px; horizontal gauge is 200px)* 

The width of the gauge area.

### `pointer` : **Object**  

The pointer configuration options.

### `pointer.border` : **Object**  

The border of the pointer.

### `pointer.border.color` : **String**  

The color of the border.Any valid CSS color string will work here, including hex and rgb.

### `pointer.border.dashType` : **String** *(default: "solid")* 

The dash type of the border.<div class="details-list">    <dl>        <dt>             <code>"solid"</code>        </dt>        <dd>             Specifies a solid line.        </dd>        <dt>             <code>"dot"</code>        </dt>        <dd>             Specifies a line consisting of dots.        </dd>        <dt>             <code>"dash"</code>        </dt>        <dd>             Specifies a line consisting of dashes.        </dd>        <dt>             <code>"longDash"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash.        </dd>        <dt>             <code>"dashDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of dash-dot.        </dd>        <dt>             <code>"longDashDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash-dot.        </dd>        <dt>             <code>"longDashDotDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash-dot-dot.        </dd>   </dl></div>

### `pointer.border.width` : **Number** *(default: 1)* 

 The width of the border.

### `pointer.color` : **String**  

The color of the pointer.

### `pointer.margin` : **Number|Object** *(default: 3)* 

 The margin of the pointer.

#### Example



    // sets the top, right, bottom and left margin to 3px.
    margin: 3
    
    // sets the top and left margin to 1px
    // margin right and bottom are with 5px (by default)
    margin: { top: 1, left: 1 }

### `pointer.opacity` : **Number** *(default: 1)* 

 The opacity of the pointer.Any valid CSS color string will work here, including hex and rgb.

### `pointer.shape` : **String**  

The shape of the pointer.<div class="details-list">    <dl>        <dt>             <code>"barIndicator"</code>        </dt>        <dd>             Specifies a filling bar indicator.        </dd>        <dt>             <code>"arrow"</code>        </dt>        <dd>             Specifies a arrow shape.        </dd>   </dl></div>

### `pointer.size` : **Number**  

The size of the pointer.

### `pointer.track` : **Object**  

The element arround/under the pointer.(available only for 'barIndicator' shape)

### `pointer.track.border` : **Object**  

The border of the track.

### `pointer.track.border.color` : **String**  

The color of the border. Any valid CSS color string will work here, including hex and rgb.

### `pointer.track.border.dashType` : **String** *(default: "solid")* 

The dash type of the border.<div class="details-list">    <dl>        <dt>             <code>"solid"</code>        </dt>        <dd>             Specifies a solid line.        </dd>        <dt>             <code>"dot"</code>        </dt>        <dd>             Specifies a line consisting of dots.        </dd>        <dt>             <code>"dash"</code>        </dt>        <dd>             Specifies a line consisting of dashes.        </dd>        <dt>             <code>"longDash"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash.        </dd>        <dt>             <code>"dashDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of dash-dot.        </dd>        <dt>             <code>"longDashDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash-dot.        </dd>        <dt>             <code>"longDashDotDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash-dot-dot.        </dd>   </dl></div>

### `pointer.track.border.width` : **Number** *(default: 1)* 

 The width of the border.

### `pointer.track.color` : **String**  

The color of the track.

### `pointer.track.opacity` : **Number**  

The opacity of the track.

### `pointer.track.size` : **Number**  

The size of the track.

### `pointer.track.visible` : **Boolean** *(default: false)* 

 The visibility of the track.

### `pointer.value` : **Number**  

The value of the gauge.

### `scale` : **Object**  

Configures the scale.

### `scale.labels` : **Object**  

Configures the scale labels.

### `scale.labels.background` : **String**  

The background color of the labels.Any valid CSS color string will work here, including hex and rgb

### `scale.labels.border` : **Object**  

The border of the labels.

### `scale.labels.border.color` : **String** *(default: "black")* 

The color of the border. Any valid CSS color string will work here, including hex and rgb.

### `scale.labels.border.dashType` : **String** *(default: "solid")* 

The dash type of the border.<div class="details-list">    <dl>        <dt>             <code>"solid"</code>        </dt>        <dd>             Specifies a solid line.        </dd>        <dt>             <code>"dot"</code>        </dt>        <dd>             Specifies a line consisting of dots.        </dd>        <dt>             <code>"dash"</code>        </dt>        <dd>             Specifies a line consisting of dashes.        </dd>        <dt>             <code>"longDash"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash.        </dd>        <dt>             <code>"dashDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of dash-dot.        </dd>        <dt>             <code>"longDashDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash-dot.        </dd>        <dt>             <code>"longDashDotDot"</code>        </dt>        <dd>             Specifies a line consisting of a repeating pattern of long-dash-dot-dot.        </dd>   </dl></div>

### `scale.labels.border.width` : **Number** *(default: 0)* 

 The width of the border.

### `scale.labels.color` : **String**  

The text color of the labels.Any valid CSS color string will work here, including hex and rgb.

### `scale.labels.font` : **String** *(default: "12px Arial,Helvetica,sans-serif")* 

The font style of the labels.

### `scale.labels.format` : **String**  

The format of the labels.

#### Example



    $("#radial-gauge").kendoLinearGauge({
        scale: {
           labels: {
               // set the format to currency
               format: "{0:C}"
           }
        }
    });

### `scale.labels.margin` : **Number|Object** *(default: 5)* 

 The margin of the labels.

#### Example



    // sets the top, right, bottom and left margin to 3px.
    margin: 3
    
    // sets the top and left margin to 1px
    // margin right and bottom are with 5px (by default)
    margin: { top: 1, left: 1 }

### `scale.labels.padding` : **Number | Object** *(default: 0)* 

 The padding of the labels.

### `scale.labels.template` : **String/Function**  

The label template.Template variables:<ul>    <li><strong>value</strong> - the value</li></ul>

#### Example



    // chart intialization
    $("#radial-gauge").kendoLinearGauge({
         scale: {
             labels: {
                 // labels template
                 template: "#= value #%"
             }
         }
    });

### `scale.labels.visible` : **Boolean** *(default: true)* 

 The visibility of the labels.

### `scale.majorTicks` : **Object**  

Configures the scale major ticks.

### `scale.majorTicks.color` : **String**  

The color of the major ticks.Any valid CSS color string will work here, including hex and rgb.

### `scale.majorTicks.size` : **Number**  

The major tick size.This is the length of the line in pixels that is drawn to indicate the tick on the scale.

### `scale.majorTicks.visible` : **Boolean** *(default: true)* 

 The visibility of the major ticks.

### `scale.majorTicks.width` : **Number** *(default: 0.5)* 

 The width of the major ticks.

### `scale.majorUnit` : **Number**  

The interval between major divisions.

### `scale.max` : **Number** *(default: 100)* 

 The maximum value of the scale.

### `scale.min` : **Number** *(default: 0)* 

 The minimum value of the scale.

### `scale.minorTicks` : **Object**  

Configures the scale minor ticks.

### `scale.minorTicks.color` : **String**  

The color of the minor ticks.Any valid CSS color string will work here, including hex and rgb.

### `scale.minorTicks.size` : **Number**  

The minor tick size.This is the length of the line in pixels that is drawn to indicate the tick on the scale.

### `scale.minorTicks.visible` : **Boolean** *(default: true)* 

 The visibility of the minor ticks.

### `scale.minorTicks.width` : **Number** *(default: 0.5)* 

 The width of the minor ticks.

### `scale.minorUnit` : **Number**  

The interval between minor divisions.

### `scale.mirror` : **Boolean**  

Mirrors the scale labels and ticks.If the labels are normally on the left side of the scale, mirroring the scale will render them to the right.

### `scale.ranges` : **Array**  

The ranges of the scale.The range fields:<div class="details-list">   <dl>        <dt>             <code>"from"</code>        </dt>        <dd>             The start position of the range in scale units.        </dd>        <dt>            <code>"to"</code>        </dt>        <dd>             The end position of the range in scale units.        </dd>        <dt>             <code>"color"</code>        </dt>        <dd>             The color of the range.Any valid CSS color string will work here, including hex and rgb.        </dd>   </dl></div>

#### Example



    $("#linear-gauge").kendoLinearGauge({
        scale: {
            ranges: [{
                from: 10,
                to: 20,
                color: "green"
            }]
        }
     });

### `scale.reverse` : **Boolean** *(default: false)* 

Reverses the axis direction - values increase from right to left and from top to bottom.

### `scale.vertical` : **Boolean**  

The position of the gauge.

### `transitions` : **Boolean** *(default: true)* 

A value indicating if transition animations should be played.



------------------------------------------

## Methods

### `redraw`()


Redraws the gauge.

#### Example

    var gauge = $("#linear-gauge").data("kendoLinearGauge");
    gauge.redraw();

### `svg`()


Returns the SVG representation of the current gauge.
The returned string is a self-contained SVG document
that can be used as is or converted to other formats
using tools like [Inkscape](http://inkscape.org/) and
[ImageMagick](http://www.imagemagick.org/).
Both programs provide command-line interface
suitable for backend processing.

#### Example

    var gauge = $("#linear-gauge").data("kendoLinearGauge");
    var svgText = gauge.svg();

### `value`()


Change the value of the gauge.

#### Example

    var gauge = $("#linear-gauge").data("kendoLinearGauge");
    gauge.redraw();



------------------------------------------

## Events

