---
title: kendo.mobile.ui.Swipe
tags: api,mobile
publish: true
---

# kendo.mobile.ui.Swipe

## Description



The mobile swipe component handles user horizontal swiping events.

### Getting Started

To register a swipe event for a given jQuery selector, use the `kendoMobileSwipe` jQuery plugin method.

#### swipe event handling

    <div>
    <p>Foo</p>
    </p>Bar</p>
    </div>
    
    <script>
     $("p").kendoMobileSwipe(function(e) {
         console.log("You swiped" + e.target.text() );
     });
    </script>

The event handler accepts a parameter with the following fields:

<table>
 <tr>
 <th align="left" valign="top">target</th>
 <td>The DOM element which was swiped</td>
 </tr>
 <tr>
 <th align="left" valign="top">direction</th>
 <td>The swipe direction. Can be either `left` or `right`.</td>
 </tr>
 <tr>
 <th align="left" valign="top">drag</th>
 <td>An instance of the kendo.Drag component, containing additional information about the drag event sequence, that generated the swipe.</td>
 </tr>
</table>



### Configuration

The swipe event criteria (minimum horizontal distance, maximum vertical deviation, timing, and swipe surface) can be configured by passing an additional parameter to the `kendoMobileSwipe` method. For more details, see the configuration section.

#### Listen only for longer and faster swipe events

    <div>
    <p>Foo</p>
    </p>Bar</p>
    </div>
    
    <script>
     $("p").kendoMobileSwipe(function(e) {
         console.log("You swiped" + e.target.text() );
     }, { minXDelta: 200, maxDuration: 100 });
    </script>

## Configuration

### maxDuration `Number`*(default: 1000)*

 The maximum amount of time in milliseconds the swipe event can last. Slower swipes are discarded.

### maxYDelta `Number`*(default: 10)*

 The maximum vertical deviation in pixels of the swipe event. Swipe with higher deviation are discarded.

### minXDelta `Number`*(default: 30)*

 The minimum horizontal distance in pixels the user should swipe before the event is triggered.

### surface `jQuery`

By default, swipe events are tracked only within the element boundries. If a surface is specified, the swipe events are extended to the provided surface. This is useful if  the swipe targets are small (or narrow).

## Methods

## Events