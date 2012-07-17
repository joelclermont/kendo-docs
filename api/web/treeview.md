---
title: kendo.ui.TreeView
slug: web-kendo.ui.treeview
tags: api,web
publish: true
---

# kendo.ui.TreeView

## Configuration

### animation `Object`

A collection of visual animations used when items are expanded or collapsed through user interaction.
Setting this option to **false** will disable all animations.

#### Example

    $("#treeView").kendoTreeView({
        animation: {
            expand: {
                duration: 200,
                hide: true,
                show: false
            },
            collapse: {
                duration: 200,
                effects: "expandVertical",
                show: true
            }
        }
    });

### animation.collapse `Animation`

The animation that will be used when collapsing items.

### animation.collapse.duration `Number`*(default: 200)*

The number of milliseconds used for the animation when a node is expanded.

#### Example

    $("#treeView").kendoTreeView({
        animation: {
            collapse: {
                duration: 1000
            }
        }
    });

### animation.collapse.effects `String`

A whitespace-delimited string of animation effects that are utilized when a **TreeView** node
is collapsed. Options include **"fadeOut"**.

#### Example

    $("#treeView").kendoTreeView({
        animation: {
            collapse: {
                duration: 5000,
                effects: "fadeOut"
            }
        }
    });

### animation.expand `Animation`

The animation that will be used when expanding items.

### animation.expand.duration `Number`*(default: 200)*

 The number of milliseconds used for the animation when a
node is expanded.

#### Example

    $("#treeView").kendoTreeView({
        animation: {
            expand: {
                duration: 1000
            }
        }
    });

### animation.expand.effects `String`*(default: "expandVertical")*

A whitespace-delimited string of animation effects that are utilized when a **TreeView** node
is expanded. Options include **"expandVertical"** and **"fadeIn"**.

#### Example

    $("#treeView").kendoTreeView({
        animation: {
            expand: {
                duration: 5000,
                effects: "expandVertical fadeIn"
            }
        }
    });

### animation.expand.show `Boolean`*(default: true)*



### checkboxTemplate `String|Function`

Template for rendering of the treeview checkboxes.

#### Example

    $("#treeview").kendoTreeView({
        template: kendo.template(
            "<input type='checkbox' name='checkedFiles[" +
                item.id +
            "]' value='true' />"
        )
    });

### dataImageUrlField `String`*(default: null)*

 Sets the field of the data item that provides
the image URL of the treeview nodes.

#### Example

    var items = [
        { id: 1, text: "Tea", image: "tea.png" },
        { id: 2, text: "Coffee", image: "coffee.png" }
    ];
    
    $("#treeview").kendoTreeView({
        dataSource: items,
        dataImageUrlField: "image"
    });

### dataSource `Array`

The data that the **TreeView** will be bound to.

### dataSpriteCssClassField `String`*(default: null)*

 Sets the field of the data item that provides
the sprite CSS class of the treeview nodes.

#### Example

    var items = [
        { id: 1, text: "Tea", sprite: "icon-tea" },
        { id: 2, text: "Coffee", sprite: "icon-coffee" }
    ];
    
    $("#treeview").kendoTreeView({
        dataSource: items,
        dataSpriteCssClassField: "sprite"
    });

### dataTextField `String`*(default: null)*

 Sets the field of the data item that provides
the text content of the treeview nodes.

#### Example

    var items = [ { id: 1, ProductName: "Tea" }, { id: 2, ProductName: "Coffee"} ];
    $("#treeview").kendoTreeView({
        dataSource: items,
        dataTextField: "ProductName"
    });

### dataUrlField `String`*(default: null)*

 Sets the field of the data item that provides
the link URL of the treeview nodes.

#### Example

    var items = [
        { id: 1, text: "Tea", LinksTo: "http://tea.example.com" },
        { id: 2, text: "Coffee", LinksTo: "http://coffee.example.com" }
    ];
    
    $("#treeview").kendoTreeView({
        dataSource: items,
        dataUrlField: "LinksTo"
    });

### dragAndDrop `Boolean`*(default: false)*

Disables (**false**) or enables (**true**) drag-and-drop on the nodes of a
**TreeView**.

### loadOnDemand `Boolean`*(default: true)*

 Indicates whether the child datasources should be fetched
lazily, when parent groups get expanded. Setting this to false causes all child dataSources to
be loaded at initialization time. Note: when initializing a TreeView from array (rather than from a
HierarchicalDataSource instance), the default value of this option is false.

### template `String|Function`

Template for rendering of the nodes of the treeview.

#### Example

    $("#treeview").kendoTreeView({
        template: "#= item.text # <a href='\\#'>Delete</a>"
    });

## Methods

### append

Appends a node to a group of a TreeView. This method may also be used to reorder the nodes of a
TreeView.

#### Append a new node with the text, "HTML5" to the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.append({ text: "HTML5" }, $("#firstItem"));

#### Moves the node with ID, secondNode as a last child of the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.append($("#secondNode"), $("#firstItem"));

#### Parameters

##### nodeData `String|Selector`

A JSON-formatted string or selector that specifies the node to be appended.

##### parentNode `Node` *(optional)*

The node that will contain the newly appended node. If not specified, the new node will be appended to the
root group of the TreeView.


### collapse

Collapses nodes.

#### Example

    var treeview = $("#treeview").data("kendoTreeView");
    
    // collapse the node with id="firstItem"
    treeview.collapse(document.getElementById("firstItem"));
    
    // collapse all nodes
    treeview.collapse(".k-item");

#### Parameters

##### nodes `Selector`

The nodes that are to be collapsed.

### dataItem

Returns the model dataItem that corresponds to a TreeView node

#### Parameters

##### node `jQueryObject | DomElement | Selector`

The element or selector that specifies a node.

### detach

Removes a node from a TreeView, but keeps its jQuery.data() objects.

#### Remove the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    var firstItem = $("#firstItem");
    firstItem.data("id", 1);
    treeview.detach(firstItem);
    firstItem.data("id") == 1;

#### Parameters

##### node `Selector`

The node that is to be detached.

#### Returns

`jQuery` The node that has been detached.

### enable

Enables or disables nodes.

#### Example

    var treeview = $("#treeview").data("kendoTreeView");
    
    // disable the node with id="firstItem"
    treeview.enable(document.getElementById("firstItem"), false);
    
    // enable all nodes
    treeview.enable(".k-item");

#### Parameters

##### nodes `Selector`

The nodes that are to be enabled/disabled.

##### enable `Boolean` *(optional, default: true)*

Whether the nodes should be enabled or disabled.

### expand

Expands nodes.

#### Example

    var treeview = $("#treeview").data("kendoTreeView");
    
    // expands the node with id="firstItem"
    treeview.expand(document.getElementById("firstItem"));
    
    // expands all nodes
    treeview.expand(".k-item");

#### Parameters

##### nodes `Selector`

The nodes that are to be expanded.

### findByText

Searches a TreeView for a node that has specific text.

#### Search a TreeView for the item that has the text, "CSS3 is da bomb!"

    var treeView = $("#treeView").data("kendoTreeView");
    var foundNode = treeView.findByText("CSS3 is da bomb!");

#### Parameters

##### text `String`

The text that is being searched for.

#### Returns

`jQuery` All nodes that have the text.

### findByUid

Searches a TreeView for a node with the given unique identifier.
Applicable when the widget is bound to a [HierarchicalDataSource](/api/framework/hierarchicaldatasource).

#### Search a TreeView for the item that has the unique id "95c1925d-a779-47fc-8420-b4274f01c037"

    var treeView = $("#treeView").data("kendoTreeView");
    var node = treeView.findByUid("95c1925d-a779-47fc-8420-b4274f01c037");

#### Parameters

##### text `String`

The text that is being searched for.

#### Returns

`jQueryObject` All nodes that have the text.

### insertAfter

Inserts a node after a specified node in a TreeView. This method may also be used to reorder the nodes of a
TreeView.

#### Insert a node with the text, "JavaScript" after the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.insertAfter({ text: "JavaScript" }, $("#firstItem"));

#### Moves a node with ID, secondNode after a node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.insertAfter($("#secondNode"), $("#firstItem"));

#### Parameters

##### nodeData `String | Selector`

A JSON-formatted string or selector that specifies the node to be inserted.

##### referenceNode `Node`

The node that will be preceed the newly-appended node.

### insertBefore

Inserts a node before another node. This method may also be used to reorder the nodes of a
TreeView.

#### Inserts a new node with the text, "CSS3" before the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.insertBefore({ text: "CSS3" }, $("#firstItem"));

#### Moves the node with ID, secondNode before the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.insertBefore($("#secondNode"), $("#firstItem"));

#### Parameters

##### nodeData `String | Selector`

A JSON-formatted string or selector that specifies the node to be inserted.

##### referenceNode `Node`

The node that follows the inserted node.

### remove

Removes a node from a TreeView.

#### Remove the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.remove($("#firstItem"));

#### Parameters

##### node `Selector`

The node that is to be removed.

### select

Gets or sets the selected node of a TreeView.

#### Select the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.select($("#firstItem"));

#### Get the currently selected node

    var treeView = $("#treeView").data("kendoTreeView");
    var selectedNode = treeView.select();

#### Parameters

##### node `Selector` *(optional)*

If provided, the node of a TreeView that should be selected.

#### Returns

`Node` The selected node of a TreeView.

### text

Gets the text of a node in a TreeView.

#### Get the text of the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    var nodeText = treeView.text($("#firstItem"));

#### Parameters

##### node `Selector`

The node of which the text is being retrieved.

#### Returns

`String` The text of a node.

### toggle

Toggles the node of a TreeView between its expanded and collapsed states.

#### Toggle the state of a node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.toggle($("#firstItem"));

#### Parameters

##### node `Selector`

The node that should be toggled.

## Events

### collapse

Triggered before a subgroup gets collapsed.

#### Event Data

##### e.node `Node`

The collapsed node

### drag

Triggered while a node is being dragged.

#### Show the user that is not permitted to drop nodes outside of the #drop-area element

    treeview.data("kendoTreeView").bind("drag", function(e) {
        if ($(e.dropTarget).parents("#drop-area").length ) {
            e.setStatusClass("k-denied");
        }
    });

#### Event Data

##### e.sourceNode `Node`

The node that is being dragged.

##### e.dropTarget `Element`

The element that the node is placed over.

##### e.pageX `Number`

The x coordinate of the mouse.

##### e.pageY `Number`

The y coordinate of the mouse.

##### e.statusClass `String`

The status that the drag clue shows.

##### e.setStatusClass `Function`

Allows a custom drag clue status to be set.


Pre-defined status classes are:

*   **k-insert-top**
        - Indicates that the item will be inserted on top.
*   **k-insert-middle**
        - Indicates that the item will be inserted in the middle.
*   **k-insert-bottom**
        - Indicates that the item will be inserted at the bottom.
*   **k-add**
        - Indicates that the item will be added/appended.
*   **k-denied**
        - Indicates an invalid operation. Using this class will automatically
          make the drop operation invalid, so there will be no need to call
          `setValid(false)` in the `drop` event.

### dragend

Triggered after a node has been dropped.

#### Event Data

##### e.sourceNode `Node`

The node that is being dropped.

##### e.destinationNode `Node`

The node that the sourceNode is being dropped upon.

##### e.dropPosition `String`

Shows where the source has been dropped. One of the values **over**, **before**, or **after**.

### dragstart

Triggered before the dragging of a node starts.

#### Disable dragging of root nodes

    treeview.data("kendoTreeView").bind("dragstart", function(e) {
        if ($(e.sourceNode).parentsUntil(".k-treeview", ".k-item").length == 0) {
            e.preventDefault();
        }
    });

#### Event Data

##### e.sourceNode `Node`

The node that will be dragged.

### drop

Triggered when a node is being dropped.

#### Event Data

##### e.sourceNode `Node`

The node that is being dropped.

##### e.destinationNode `Node`

The node that the sourceNode is being dropped upon.

##### e.valid `Boolean`

Whether this drop operation is permitted.

##### e.setValid `Function`

Allows the drop to be prevented.

##### e.dropTarget `Element`

The element that the node is placed over.

##### e.dropPosition `String`

Shows where the source will be dropped. One of the values **over**, **before**, or **after**.

### expand

Triggered before a subgroup gets expanded.

#### Event Data

##### e.node `Node`

The expanded node

### select

Triggered when a node gets selected.

#### Event Data

##### e.node `Node`

The selected node
