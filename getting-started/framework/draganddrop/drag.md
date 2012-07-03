---
title: Drag Component
slug: drag-component
publish: true
---

# Drag Component

The Kendo.Drag component provides a cross-browser, touch-friendly way to handle mouse and touch drag events.

## Getting Started

The kendo.Drag constructor accepts an element and a object with configuration options. Review the API reference for a full list of the configuration options.
  

#### Initialize Kendo.Drag instance
 
    var drag = new Kendo.Drag($("#foo"), {
    start: function(e) { ... },
    move: function(e) { ... },
    // ...
    })
      

## Drag Event Lifecycle

The Drag component raises five events: `start`, `move`, `end`, `tap`, `cancel`.

An important thing to notice is that the `start` event gets fired after the _first_ `mousemove`/`touchmove` event.
This allows detection of accidental short mouse/finger drag events.

Once a `start` event is fired, `move` and `end` events are guaranteed to be fired.
The only exception is the case when the consumer of the events cancels the event lifecycle using the `cancel` _method_. In this case, the `cancel` _event_ gets fired.

If the user presses and releases the mouse (or the equivalent gesture on touch enabled devices) without any movement,
or the movement distance is below the threshold specified, the `tap` event is fired.

## DOM Event Cancellation

By default, the Drag component does not call `preventDefault` on any of the DOM events it binds to. However, there are several cases where this might be necessary, for example:

*   To prevent default scrolling on touch devices;
*   To avoid text selection when dragging elements. 

To prevent the default effect of the respective DOM events, the event handler can call `preventDefault` on the Drag event parameter.
  

#### Prevent default browser behavior on mousemove/touchmove
 
    var drag = new Kendo.Drag($("#foo"));
    
    drag.bind("move", function(e) {
    e.preventDefault();
    });
      

## Drag Event Coordinates and Information

In each event handler, the Drag component passes its data in the event handler parameter. The event information is grouped in two axis object instances — `x` and `y`.
Each axis instance has the following fields:

*   `location` - the offset of the mouse/touch relative to the _entire document_ (pageX/Y);
*   `startLocation` - the offset of the mouse/touch relative to the document when the drag started;
*   `client` - the offset of the mouse/touch relative to the _viewport_ (clientX/Y);
*   `delta` - the change from the previous event location
*   `velocity` - the pixels per millisecond speed of the current move.
For instance, the mobile ScrollView widget considers a drag with velocity below 0.8 a slow one, while velocity above 1.6 is a fast one.  

#### Access event coordinates in drag move event
 
    var drag = new Kendo.Drag($("#foo"));
    
    drag.bind("move", function(e) {
    console.log(e.x.location);
    console.log(e.y.location);
    });
      

## Handle Dragging Outside the Element Boundaries

If the Drag component is bound to a small DOM element, the mouse finger may leave element boundaries while dragging.
In this case, by default, the Drag component will trigger the `end` event.
The `global` configuration option would cause the drag to track the events for the entire document surface until the mouse is released.
This is the behavior of the kendo Draggable widget.
  

#### Handle drag events for the entire document.
 
    var drag = new Kendo.Drag($("#foo"), { global: true });
      

## Nest Elements with Drag Listeners

If several Drag components are bound to nested elements, dragging the innermost element will trigger multiple drag events as the DOM events bubble.
To prevent this behavior, call the drag `capture` method in the `start` event handler.
  

#### Capture innermost drag event
 
    <div id="foo">
    <div id="bar">
    
    </div>
    
    <script>
    var drag = new Kendo.Drag($("#bar"), {
    start: function(e) {
        e.capture();
    }
    });
    
    // This drag won't trigger any events, as the inner element captures every drag.
    var drag = new Kendo.Drag($("#foo"));
    </script>
     </div> 

## Cancel Drag Event Cycle

In some conditions the drag event consumer may decide not to handle the current drag.
For instance, the mobile ScrollView skips handling of vertical drag gestures.
In this case, the drag `cancel` method can be used. Once this method is called, the drag instance raises `cancel` event.
_No subsequent_ `move` and `end` events are raised for that drag gesture.
  

#### Cancel drag event lifecycle
 
    var drag = new Kendo.Drag($("#foo"), {
    start: function(e) {
        e.cancel();
    }
    });
     