## Description


kendo.ui.TreeView.Description

 The **TreeView** displays hierarchical data in a traditional tree structure. It supports user
 interaction through the mouse or touch to perform re-ordering operations via drag-and-drop.



 A **TreeView** can be created by leveraging HTML lists. However, it does not support binding to a
 remote data source at this point in time.


### Getting Started

A **TreeView** can be created in two ways:

1.  Define a hierarchical list with static HTML
2.  Use dynamic data binding



 Static HTML definition is appropriate for small hierarchies and for data that does not change frequently.
 Databinding should be used for larger data sets and for data that changes frequently.


### Creating a TreeView from HTML

#### Create a hierarchical list in HTML

    <ul id="treeView">
        <li>Item 1
            <ul>
                <li>Item 1.1</li>
                <li>Item 1.2</li>
            </ul>
        </li>
        <li>Item 2</li>
    </ul>


 Initialization of a **TreeView** should occur after the DOM is fully loaded. It is recommended
 that initialization the **TreeView** occur within a handler is provided to $(document).ready().

#### Initialize a TreeView using a selector within $(document).ready()

    $(document).ready(function() {
        $("#treeView").kendoTreeView();
    });


### Creating a TreeView with Data Binding to a Local Data Source

#### Create a hierarchical HTML list

    <div id="treeView"></div>


#### Initialize and bind the TreeView

    $(document).ready(function() {
        $("#treeView").kendoTreeView({
            dataSource: [
                {
                    text: "Item 1",
                    items: [
                        { text: "Item 1.1" },
                        { text: "Item 1.2" }
                    ]
                },
                { text: "Item 2" }
            ]
        })
    });


Currently, the **TreeView** does not support binding to a remote data source.

#### TreeView item JSON structure

    var item = {
        text: "Item text",
    
        // renders a <img class="k-image" src="/images/icon.png" />
        imageUrl: "/images/icon.png",
    
        // renders a <span class="k-sprite icon save" />
        spriteCssClass: "icon save",
    
        // specifies whether the node text should be encoded or not
        // useful when rendering node-specific HTML
        encoded: false,
    
        items: [
            // child items
        ]
    }


### Configuring TreeView Behavior


 A number of **TreeView** behaviors can be easily controlled by simple configuration properties,
 such as animation behaviors and drag-and-drop behaviors.

#### Enabling drag-and-drop for TreeView nodes

    $("#treeView").kendoTreeView({
        dragAndDrop: true
    });


 When drag-and-drop is enabled, the nodes of a **TreeView** can be dragged and dropped between all
 levels, with useful tooltips helping indicate where the node will be dropped.


### Accessing an Existing TreeView


 You can reference an existing **TreeView** instance via
 [jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
 use the API to control its behavior.

#### Accessing an existing TreeView instance

    var treeView = $("#treeView").data("kendoTreeView");



------------------------------------------

## Configuration

### `animation` : **Object**  

A collection of visual animations used when items are expanded or collapsed through user interaction.Setting this option to <strong>false</strong> will disable all animations.

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

### `animation.collapse` : **Animation**  

The animation that will be used when collapsing items.

### `animation.collapse.duration` : **Number** *(default: 200)* 

The number of milliseconds used for the animation when a node is expanded.

#### Example



    $("#treeView").kendoTreeView({
        animation: {
            collapse: {
                duration: 1000
            }
        }
    });

### `animation.collapse.effects` : **String**  

A whitespace-delimited string of animation effects that are utilized when a <strong>TreeView</strong> nodeis collapsed. Options include <strong>"fadeOut"</strong>.

#### Example



    $("#treeView").kendoTreeView({
        animation: {
            collapse: {
                duration: 5000,
                effects: "fadeOut"
            }
        }
    });

### `animation.expand` : **Animation**  

The animation that will be used when expanding items.

### `animation.expand.duration` : **Number** *(default: 200)* 

 The number of milliseconds used for the animation when anode is expanded.

#### Example



    $("#treeView").kendoTreeView({
        animation: {
            expand: {
                duration: 1000
            }
        }
    });

### `animation.expand.effects` : **String** *(default: "expandVertical")* 

A whitespace-delimited string of animation effects that are utilized when a <strong>TreeView</strong> nodeis expanded. Options include <strong>"expandVertical"</strong> and <strong>"fadeIn"</strong>.

#### Example



    $("#treeView").kendoTreeView({
        animation: {
            expand: {
                duration: 5000,
                effects: "expandVertical fadeIn"
            }
        }
    });

### `animation.expand.show` : **Boolean** *(default: true)* 



### `checkboxTemplate` : **String|Function**  

Template for rendering of the treeview checkboxes.

#### Example



    $("#treeview").kendoTreeView({
        template: kendo.template(
            "<input type='checkbox' name='checkedFiles[" +
                item.id +
            "]' value='true' />"
        )
    });

### `dataSource` : **Array**  

The data that the <strong>TreeView</strong> will be bound to.

### `dragAndDrop` : **Boolean** *(default: false)* 

Disables (<strong>false</strong>) or enables (<b>true</b>) drag-and-drop on the nodes of a<strong>TreeView</strong>.

### `template` : **String|Function**  

Template for rendering of the nodes of the treeview.

#### Example



    $("#treeview").kendoTreeView({
        template: "#= item.text # <a href='\\#'>Delete</a>"
    });



------------------------------------------

## Methods

### `append`(nodeData, parentNode)


Appends a node to a group of a TreeView. This method may also be used to reorder the nodes of a
TreeView.

#### Append a new node with the text, "Meanwhile, in HTML5..." to the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.append({ text: "Meanwhile, in HTML5..." }, $("#firstItem"));


#### Moves the node with ID, secondNode as a last child of the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.append($("#secondNode"), $("#firstItem"));

#### Parameters 

##### nodeData `String|Selector`

A JSON-formatted string or selector that specifies the node to be appended.

##### parentNode `Node`

_optional, default: _

The node that will contain the newly appended node. If not specified, the new node will be appended to the
root group of the TreeView.

### `collapse`(nodes)


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

### `detach`(node)`jQueryObject`


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

`jQueryObject` The node that has been detached.

### `enable`(nodes, enable)


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

##### enable `Boolean`

_optional, default: true_

Whether the nodes should be enabled or disabled.

### `expand`(nodes)


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

### `findByText`(text)`jQueryObject`


Searches a TreeView for a node that has specific text.

#### Search a TreeView for the item that has the text, "CSS3 is da bomb!"

    var treeView = $("#treeView").data("kendoTreeView");
    var foundNode = treeView.findByText("CSS3 is da bomb!");

#### Parameters 

##### text `String`

The text that is being searched for.

#### Returns 

`jQueryObject` All nodes that have the text.

### `insertAfter`(nodeData, referenceNode)


Inserts a node after a specified node in a TreeView. This method may also be used to reorder the nodes of a
TreeView.

#### Insert a node with the text, "Y U NO insert node?" after the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.insertAfter({ text: "Y U NO insert node?" }, $("#firstItem"));


#### Moves a node with ID, secondNode after a node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.insertAfter($("#secondNode"), $("#firstItem"));

#### Parameters 

##### nodeData `String|Selector`

A JSON-formatted string or selector that specifies the node to be inserted.

##### referenceNode `Node`

The node that will be preceed the newly-appended node.

### `insertBefore`(nodeData, referenceNode)


Inserts a node before another node. This method may also be used to reorder the nodes of a
TreeView.

#### Inserts a new node with the text, "It's over 9000!" before the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.insertBefore({ text: "It's over 9000!" }, $("#firstItem"));


#### Moves the node with ID, secondNode before the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.insertBefore($("#secondNode"), $("#firstItem"));

#### Parameters 

##### nodeData `String|Selector`

A JSON-formatted string or selector that specifies the node to be inserted.

##### referenceNode `Node`

The node that follows the inserted node.

### `remove`(node)


Removes a node from a TreeView.

#### Remove the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.remove($("#firstItem"));

#### Parameters 

##### node `Selector`

The node that is to be removed.

### `select`(node)`Node`


Gets or sets the selected node of a TreeView.

#### Select the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.select($("#firstItem"));


#### Get the currently selected node

    var treeView = $("#treeView").data("kendoTreeView");
    var selectedNode = treeView.select();

#### Parameters 

##### node `Selector`

_optional, default: _

If provided, the node of a TreeView that should be selected.

#### Returns 

`Node` The selected node of a TreeView.

### `text`(node)`String`


Gets the text of a node in a TreeView.

#### Get the text of the node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    var nodeText = treeView.text($("#firstItem"));

#### Parameters 

##### node `Selector`

The node of which the text is being retrieved.

#### Returns 

`String` The text of a node.

### `toggle`(node)


Toggles the node of a TreeView between its expanded and collapsed states.

#### Toggle the state of a node with ID, firstItem

    var treeView = $("#treeView").data("kendoTreeView");
    treeView.toggle($("#firstItem"));

#### Parameters 

##### node `Selector`

The node that should be toggled.



------------------------------------------

## Events

### `collapse`
Triggered before a subgroup gets collapsed.

kendo.ui.TreeView#collapse


#### Event Data 

##### e.node `Node`

The collapsed node

### `drag`
Triggered while a node is being dragged.

kendo.ui.TreeView#drag



#### Show the user that is not permitted to drop nodes outside of the #drop-area element

    treeview.data("kendoTreeView").bind("drag", function(e) {
        if ($(e.dropTarget).parents("#drop-area").length ) {
            e.setStatusClass("k-denied");
        }
    });

#### Event Data 

##### e.sourceNode `Node`

The node that is being dragged.

##### e.dropTarget `DomElement`

The element that the node is placed over.

##### e.pageX `Integer`

The x coordinate of the mouse.

##### e.pageY `Integer`

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

### `dragend`
Triggered after a node has been dropped.

kendo.ui.TreeView#dragend


#### Event Data 

##### e.sourceNode `Node`

The node that is being dropped.

##### e.destinationNode `Node`

The node that the sourceNode is being dropped upon.

##### e.dropPosition `String`

Shows where the source has been dropped. One of the values **over**, **before**, or **after**.

### `dragstart`
Triggered before the dragging of a node starts.

kendo.ui.TreeView#dragstart



#### Disable dragging of root nodes

    treeview.data("kendoTreeView").bind("dragstart", function(e) {
        if ($(e.sourceNode).parentsUntil(".k-treeview", ".k-item").length == 0) {
            e.preventDefault();
        }
    });

#### Event Data 

##### e.sourceNode `Node`

The node that will be dragged.

### `drop`
Triggered when a node is being dropped.

kendo.ui.TreeView#drop


#### Event Data 

##### e.sourceNode `Node`

The node that is being dropped.

##### e.destinationNode `Node`

The node that the sourceNode is being dropped upon.

##### e.valid `Boolean`

Whether this drop operation is permitted.

##### e.setValid `Function`

Allows the drop to be prevented.

##### e.dropTarget `DomElement`

The element that the node is placed over.

##### e.dropPosition `String`

Shows where the source will be dropped. One of the values **over**, **before**, or **after**.

### `expand`
Triggered before a subgroup gets expanded.

kendo.ui.TreeView#expand


#### Event Data 

##### e.node `Node`

The expanded node

### `select`
Triggered when a node gets selected.

kendo.ui.TreeView#select


#### Event Data 

##### e.node `Node`

The selected node

