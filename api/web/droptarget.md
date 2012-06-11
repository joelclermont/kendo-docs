# kendo.ui.DropTarget

## Configuration

### `group` : **String** *(default: "default")*

 Used to group sets of draggable and drop targets. A draggable with the same group value as a drop target will be accepted by the drop target.

## Methods

## Events

### dragenter

Fires when draggable moves over the drop target.

#### Event Data

##### e.draggable `jQuery`

Reference to the draggable that enters the drop target.

### dragleave

Fires when draggable moves out of the drop target.

#### Event Data

##### e.draggable `jQuery`

Reference to the draggable that leaves the drop target.

### drop

Fires when draggable is dropped over the drop target.

#### Event Data

##### e.draggable `jQuery`

Reference to the draggable that is dropped over the drop target.

##### e.draggable.currentTarget `jQuery`

The element that the drag and drop operation started from.