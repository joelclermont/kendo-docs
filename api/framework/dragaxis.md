---
title: kendo.DragAxis
slug: fw-kendo.dragaxis
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


*   **location** - the offset of the mouse/touch relative to the _entire document_ (pageX/Y);
*   **startLocation** - the offset of the mouse/touch relative to the document when the drag started;
*   **client** - the offset of the mouse/touch relative to the _viewport_ (clientX/Y);
*   **delta** - the change from the previous event location
*   **velocity** - the pixels per millisecond speed of the current move. For instance, the mobile ScrollView widget considers a drag with velocity below 0.8 a slow one, while velocity above 1.6 is a fast one.
