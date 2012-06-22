---
title: kendo.ui.ListView
tags: api,web
publish: true
---

# kendo.ui.ListView

## Description



      The ListView is designed to give your the freedom to specify custom type of layout
      for the items displayed in the control. It can be bound to local JSON data or to
      remote data using the Kendo DataSource component.
 

### Getting Started

#### Creating a **ListView** from existing HTML element

      <ul id="listView"></ul>

#### Initialize the Kendo Grid

      $(document).ready(function(){
          $("#listView").kendoListView({
              template: "<li>${FirstName} ${LastName}</li>",
              dataSource: {
                  data: [
                      {
                          FirstName: "Joe",
                          LastName: "Smith"
                      },
                      {
                          FirstName: "Jane",
                          LastName: "Smith"
                  }]
              }
          });
      });

### Configuring ListView Behavior

 Kendo ListView supports paging, selection, navigation, editing. Configuring any of
 these ListView behaviors is done using simple boolean configuration options. For
 example, the follow snippet shows how to enable all of these behaviors.

#### Enabling ListView paging, selection, navigation and editing

       $(document).ready(function(){
          $("#listView").kendoListView({
             pageable: true,
             selectable: true,
             navigatable: true,
             editable: true,
             template: "<li>${FirstName}</li>",
             editTemplate: '<li><input type="text" data-bind="value:FirstName" name="FirstName" required="required"/></li>'
          });
      });

By default, paging, selection, navigation and editing are **disabled**.

## Configuration

### `autoBind` : **Boolean** *(default: true)*

 Indicates whether the list view will call read on the DataSource initially.

#### Example

    $("#listView").kendoListView({
         dataSource: {
             data: createRandomData(50)
         },
         template: "<li>${Name} ${BirthDate}</li>",
         autoBind: false // the list view will not be populated with data until read() is called on the sharedDataSource
     });

### `dataSource` : **kendo.data.DataSource | Object** 

Instance of DataSource or Object with DataSource configuration.

#### Example

    var sharedDataSource = new kendo.data.DataSource({
         data: [{title: "Star Wars: A New Hope", year: 1977}, {title: "Star Wars: The Empire Strikes Back", year: 1980}],
         pageSize: 1
    });
    
    $("#listView").kendoListView({
         dataSource: sharedDataSource,
         template: "<li>${title} ${year}</li>"
     });

#### Example

    $("#listView").kendoListView({
         dataSource: {
             data: [{title: "Star Wars: A New Hope", year: 1977}, {title: "Star Wars: The Empire Strikes Back", year: 1980}],
             template: "<li>${title} ${year}</li>"
         }
     });

### `editTemplate` : **Function** 

Specifies ListView item template in edit mode.

#### Example

    <script type="text/x-kendo-tmpl" id="template">
         <div>
           <dl>
             <dt>Name</dt> <dd>${Name}</dd>
             <dt>Age</dt> <dd>${Age}</dd>
           </dl>
         </div>
     </script>
    
     <script type="text/x-kendo-tmpl" id="editTemplate">
         <div>
           <dl>
             <dt>Name</dt>
             <dd><input type="text" data-bind="value:Name" name="Name" required="required" /></dd>
             <dt>Age</dt>
             <dd><input type="text" data-bind="value:Age" data-role="numerictextbox" data-type="number" name="Age" required="required /></dd>
           </dl>
         </div>
     </script>

#### Example

    $("#listView").kendoListView({
         dataSource: {
             data: createRandomData(50)
         },
         template: kendo.template($("#template").html()),
         editTemplate: kendo.template($("#editTemplate").html())
     });

### `navigatable` : **Boolean** *(default: false)*

 Indicates whether keyboard navigation is enabled/disabled.

#### Example

    $("#listView").kendoListView({
         dataSource: {
             data: createRandomData(50),
         },
         template: "<li>${Name} ${BirthDate}</li>",
         navigatable: true
     });

### `selectable` : **String** *(default: false)*

 Indicates whether selection is enabled/disabled. Possible values:
<div class="details-list">
   <dl>
        <dt>
             **true**
        </dt>
        <dd>
             Single item selection.
        </dd>
        <dt>
             **"single"**
        </dt>
        <dd>
             Single item selection.
        </dd>
        <dt>
             **"multiple"**
        </dt>
        <dd>
             Multiple item selection.
        </dd>
   </dl>
</div>

### `template` : **Function** 

Specifies ListView item template.

#### Example

    <script type="text/x-kendo-tmpl" id="template">
         <div>
           <dl>
             <dt>Name</dt> <dd>${Name}</dd>
             <dt>Birth Date</dt> <dd>${BirdthDate}</dd>
           </dl>
         </div>
     </script>

#### Example

    $("#listView").kendoListView({
         dataSource: {
             data: createRandomData(50)
         },
         template: kendo.template($("#template").html())
     });

## Methods

### add

Inserts empty item as first item on the current view and prepare it for editing.

#### Example

    // get a reference to the list view widget
    var listView = $("#listView").data("kendoListView");
    // add item
    listView.add();

### cancel

Cancels changes in currently edited item.

#### Example

    // get a reference to the list view widget
    var listView = $("#listView").data("kendoListView");
    // cancel changes in currently edited item
    listView.cancel();

### clearSelection

Clears ListView selected items and triggers change event.

### edit

Edit specified ListView item. Triggers edit event.

#### Example

    // get a reference to the list view widget
    var listView = $("#listView").data("kendoListView");
    // edit first list view item
    listView.edit(listView.element.children().first());

#### Parameters

##### item `Object`

jQuery object containing the item to be edited.

### refresh

Reloads the data and repaints the list view.

#### Example

    var listView = $("#listView").data("kendoListView");
    
    // refreshes the list view
    listView.refresh();

### remove

Removes specified ListView item. Triggers remove event and if not prevented calls DataSource sync method.

#### Example

    // get a reference to the list view widget
    var listView = $("#listView").data("kendoListView");
    // remove first list view item
    listView.remove(listView.element.children().first());

#### Parameters

##### item `Object`

jQuery object containing the item to be removed.

### save

Saves edited ListView item. If validation succeeds will call DataSource sync method.

#### Example

    // get a reference to the list view widget
    var listView = $("#listView").data("kendoListView");
    // edit first list view item
    listView.edit(listView.element.children().first());
    // save edited item
    listView.save();

### select

Selects the specified ListView item. If called without arguments - returns the selected items.

#### Example

    // get a reference to the list view widget
    var listView = $("#listView").data("kendoListView");
    // selects first list view item
    listView.select(listView.element.children().first());

#### Parameters

##### items `Selector | Array`

Items to select.

## Events

### change

Fires when the list view selection has changed.

#### Example

     $("#listView").kendoListView({
         change: function(e) {
             // handle event
         }
     });

#### To set after initialization

     // get a reference to the list view
     var listView = $("#listView").data("kendoListView");
     // bind to the change event
     listView.bind("change", function(e) {
         // handle event
     }

### dataBound

Fires when the list view has received data from the data source.
and is about to render it.

#### Example

    function onDataBound(e) {
        // handle event
    }

### edit

Fires when the list view enters edit mode.

#### Example

     $("#listView").kendoListView({
         edit: function(e) {
             // handle event
     });

#### To set after initialization

     // get a reference to the list view
     var listView = $("#listView").data("kendoListView");
     // bind to the edit event
     listView.bind("edit", function(e) {
         // handle event
     }

#### Event Data

##### e.item `Object`

The jQuery element to be edited.

##### e.model `Object`

The model to be edited.

### remove

Fires before the list view item is removed.

#### Example

     $("#listView").kendoListView({
         remove: function(e) {
             // handle event
     });

#### To set after initialization

     // get a reference to the list view
     var listView = $("#listView").data("kendoListView");
     // bind to the remove event
     listView.bind("remove", function(e) {
         // handle event
     }

#### Event Data

##### e.item `Object`

The item element to be deleted.

##### e.model `Object`

The model which to be deleted.