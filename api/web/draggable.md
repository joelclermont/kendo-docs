---title: kendo.ui.Draggable
tags: api,web
publish: true
---
# kendo.ui.Draggable

## Description



#### Draggable

Enable draggable functionality on any DOM element.

#### **Draggable** initialization

    var draggable = $("#draggable").kendoDraggable();

#### DropTarget

Enable any DOM element to be a target for draggable elements.

#### **DropTarget** initialization

    var dropTarget = $("#dropTarget").kendoDropTarget();

## Configuration

### `axis` : **String** *(default: null)*

 Constrains the hint movement to either the horizontal (x) or vertical (y) axis. Can be set to either "x" or "y".

### `container` : **jQuery** 

If set, the hint movement is constrained to the container boundaries.

### `cursorOffset` : **Object** *(default: null)*

 If set, specifies the offset of the hint relative to the mouse cursor/finger.
By default, the hint is initially positioned on top of the draggable source offset. The option accepts an object with two keys: `top` and `left`.

#### Example

    $("#draggable").kendoDraggable({cursorOffset: {top: 10, left: 10}});

### `distance` : **Number** *(default: 5)*

 The required distance that the mouse should travel in order to initiate a drag.

### `filter` : **Selector** 

Selects child elements that are draggable if a widget is attached to a container.

### `group` : **String** *(default: "default")*

 Used to group sets of draggable and drop targets. A draggable with the same group value as a drop target will be accepted by the drop target.

### `hint` : **Function | jQuery** 

Provides a way for customization of the drag indicator. If a function is supplied, it receives one argument - the draggable element's jQuery object.

#### Example

    //hint as a function
     $("#draggable").kendoDraggable({
         hint: function(element) {
             return $("#draggable").clone();
             // same as
             //  return element.clone();
         }
     });
    
    //hint as jQuery object
     $("#draggable").kendoDraggable({
         hint: $("#draggableHint");
     });

## Methods

## Events

### drag

Fires while dragging.

### dragcancel

Fires when item drag is canceled by pressing the Escape key.

### dragend

Fires when item drag ends.

### dragstart

Fires when item drag starts.