---title: kendo.DragAxis
tags: api,framework
publish: true
---
# kendo.DragAxis

## Description



#### DragAxis

The DragAxis is used internally by the kendo.Drag component to store and calculate event data.
The Drag component contains two DragAxis instances: `x` for the horizontal coordinates, and `y` for the vertical.
The two DragAxis instances are available in each Drag event parameter.

#### Access DragAxis information in Drag start event

    new kendo.Drag($("#foo"), {
     start: function(e) {
         console.log(x); // Horizontal axis
         console.log(y); // Vertical axis
     }
    });

Each axis instance contains the following fields:


*   **location** - the offset of the mouse/touch relative to the entire document (pageX/Y);
*   **startLocation** - the offset of the mouse/touch relative to the document when the drag started;
*   **client** - the offset of the mouse/touch relative to the viewport (clientX/Y);
*   **delta** - the change from the previous event location
*   **velocity** - the pixels per millisecond speed of the current move.

## Configuration

## Methods

## Events