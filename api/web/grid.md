---title: kendo.ui.Grid
tags: api,web
publish: true
---
# kendo.ui.Grid

## Description



     The Grid widget displays tabular data and offers rich support interacting with data,
     including paging, sorting, grouping, and selection. Grid is a powerful widget with
     many configuration options. It can be bound to local JSON data or to remote data
     using the Kendo DataSource component.
 

### Getting Started

 There are two primary ways to create a Kendo Grid:

 

1.  From an existing HTML table element, defining columns, rows, and data in HTML
2.  From an HTML div element, defining columns and rows with configuration, and binding to data

#### Creating a **Grid** from existing HTML Table element

     <!-- Define the HTML table, with rows, columns, and data -->
     <table id="grid">
      <thead>
          <tr>
              <th data-field="title">Title</th>
              <th data-field="year">Year</th>
          </tr>
      </thead>
      <tbody>
          <tr>
              <td>Star Wars: A New Hope</td>
              <td>1977</td>
          </tr>
          <tr>
              <td>Star Wars: The Empire Strikes Back</td>
              <td>1980</td>
          </tr>
      </tbody>
     </table>

#### Initialize the Kendo Grid

      $(document).ready(function(){
          $("#grid").kendoGrid();
      });

#### Creating a **Grid** from existing HTML Div element

     <!-- Define the HTML div that will hold the Grid -->
     <div id="grid">
     </div>

#### Initialize the Kendo Grid and configure columns & data binding

       $(document).ready(function(){
          $("#grid").kendoGrid({
              columns:[
                  {
                      field: "FirstName",
                      title: "First Name"
                  },
                  {
                      field: "LastName",
                      title: "Last Name"
              }],
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

### Configuring Grid Behavior

 Kendo Grid supports paging, sorting, grouping, and scrolling. Configuring any of
 these Grid behaviors is done using simple boolean configuration options. For
 example, the follow snippet shows how to enable all of these behaviors.

#### Enabling Grid paging, sorting, grouping, and scrolling

       $(document).ready(function(){
          $("#grid").kendoGrid({
             groupable: true,
             scrollable: true,
             sortable: true,
             pageable: true
          });
      });

By default, paging, grouping, and sorting are **disabled**. Scrolling is enabled by default.

 

### Performance with Virtual Scrolling

 When binding to large data sets or when using large page sizes, reducing active in-memory
 DOM objects is important for performance. Kendo Grid provides built-in UI virtualization
 for highly optimized binding to large data sets. Enabling UI virtualization is done via simple configuration.

#### Enabling Grid UI virtualization

       $(document).ready(function(){
          $("#grid").kendoGrid({
             scrollable: {
                 virtual: true
             }
          });
      });

### Accessing an Existing Grid


 You can reference an existing **Grid** instance via
 [jQuery.data()](http://api.jquery.com/jQuery.data/).
 Once a reference has been established, you can use the API to control
 its behavior.

#### Accessing an existing Grid instance

    var grid = $("#grid").data("kendoGrid");

## Configuration

### `autoBind` : **Boolean** *(default: true)*

 Indicates whether the grid will call read on the DataSource initially.

#### Example

    $("#grid").kendoGrid({
         dataSource: sharedDataSource,
         columns: [
             {
                 field: "Name"
             },
             {
                 field: "BirthDate",
                 title: "Birth Date",
                 template: '#= kendo.toString(BirthDate,"dd MMMM yyyy") #'
            }
         ],
         autoBind: false // the grid will not be populated with data until read() is called on the sharedDataSource
     });

### `columns` : **Array** 

A collection of column objects or collection of strings that represents the name of the fields.

#### Example

    var sharedDataSource = new kendo.data.DataSource({
         data: [{title: "Star Wars: A New Hope", year: 1977}, {title: "Star Wars: The Empire Strikes Back", year: 1980}],
         pageSize: 1
    });
    $("#grid").kendoGrid({
        dataSource: sharedDataSource,
        columns: [ { title: "Action", command: "destroy" }, // creates a column with delete buttons
                   { title: "Title", field: "title", width: 200, template: "<div id='title'>${ title }</div>" },
                   { title: "Year", field: "year", filterable: false, sortable: true, format: "{0:dd/MMMM/yyyy}" } ];
    });

### `columns.command` : **String** 

Definition of command column. The supported built-in commands are: "create", "cancel", "save", "destroy".

### `columns.editor` : **Function** 

Provides a way to specify custom editor for this column.

#### Example

    $(".k-grid").kendoGrid({
         dataSource: {
             data: createRandomData(50)
         },
         editable: true,
         columns: [
             {
                 field: "Name",
                 editor: function(container, options) {
                     // create a KendoUI AutoComplete widget as column editor
                      $('<input name="' + options.field + '"/>')
                          .appendTo(container)
                          .kendoAutoComplete({
                              dataTextField: "ProductName",
                              dataSource: {
                                  transport: {
                                    //...
                                  }
                              }
                          });
                 }
             }
         ]
      });

### `columns.editor.container` : **Object** 

The container in which the editor must be added.

### `columns.editor.options` : **Object** 

Additional options.

### `columns.editor.options.field` : **String** 

The field for the editor.

### `columns.editor.options.model` : **Object** 

The model for the editor.

### `columns.encoded` : **Boolean** *(default: true)*

 Specified whether the column content is escaped. Disable encoding if the data contains HTML markup.

### `columns.field` : **String** 

The field from the datasource that will be displayed in the column.

### `columns.filterable` : **Boolean** *(default: true)*

 Specifies whether given column is filterable.

### `columns.format` : **String** 

The format that will be applied on the column cells.

#### Example

    $("#grid").kendoGrid({
         dataSource: {
             data: createRandomData(50),
             pageSize: 10
         },
         columns: [
             {
                 field: "BirthDate",
                 title: "Birth Date",
                 format: "{0:dd/MMMM/yyyy}"
            }
         ]
      });

### `columns.sortable` : **Boolean** *(default: true)*

 Specifies whether given column is sortable.

### `columns.template` : **String** 

The template for column's cells.

#### Example

    $("#grid").kendoGrid({
         dataSource: {
             data: createRandomData(50),
             pageSize: 10
         },
         columns: [
             {
                 field: "Name"
             },
             {
                 field: "BirthDate",
                 title: "Birth Date",
                 template: '#= kendo.toString(BirthDate,"dd MMMM yyyy") #'
            }
         ]
      });

### `columns.title` : **String** 

The text that will be displayed in the column header.

### `columns.width` : **String** 

The width of the column.

### `dataSource` : **kendo.data.DataSource | Object** 

Instance of DataSource or Object with DataSource configuration.

#### Example

    var sharedDataSource = new kendo.data.DataSource({
         data: [{title: "Star Wars: A New Hope", year: 1977}, {title: "Star Wars: The Empire Strikes Back", year: 1980}],
         pageSize: 1
    });
    
    $("#grid").kendoGrid({
         dataSource: sharedDataSource
     });

#### Example

    $("#grid").kendoGrid({
         dataSource: {
             data: [{title: "Star Wars: A New Hope", year: 1977}, {title: "Star Wars: The Empire Strikes Back", year: 1980}],
             pageSize: 1
         }
     });

### `detailTemplate` : **Function** 

Template to be used for rendering the detail rows in the grid.
See the [**Detail Template**](http://demos.kendoui.com/web/grid/detailtemplate.html) example.

### `editable` : **Object** 

Indicates whether editing is enabled/disabled.

#### Example

    $("#grid").kendoGrid({
         dataSource: {
             data: createRandomData(50),
             pageSize: 10
         },
         columns: [
             {
                 field: "Name"
             },
             {
                 field: "BirthDate",
                 title: "Birth Date",
                 template: '#= kendo.toString(BirthDate,"dd MMMM yyyy") #'
            }
         ]
         toolbar: [
             "create",
             { name: "save", text: "Save This Record" },
             { name: "cancel", template: "<img src="icons/cancel.png' rel='cancel' />" }
         ],
         editable: {
             update: true, // puts the row in edit mode when it is clicked
             destroy: false, // does not remove the row when it is deleted, but marks it for deletion
             confirmation: "Are you sure you want to remove this item?"
         }
     });

### `editable.confirmation` : **Boolean | String** 

Defines the text that will be used in confirmation box when delete an item.

### `editable.destroy` : **Boolean** 

Indicates whether item should be deleted when click on delete button.

### `editable.mode` : **String** 

Indicates which of the available edit modes(incell(default)/inline/popup) will be used

### `editable.template` : **String** 

Template which will be use during popup editing

### `editable.update` : **Boolean** 

Indicates whether item should be switched to edit mode on click.

### `groupable` : **Boolean** *(default: false)*

 Indicates whether grouping is enabled/disabled.

#### Example

    $("#grid").kendoGrid({
         dataSource: {
             data: createRandomData(50),
             pageSize: 10
         },
         columns: [
             {
                 field: "Name"
             },
             {
                 field: "BirthDate",
                 title: "Birth Date",
                 template: '#= kendo.toString(BirthDate,"dd MMMM yyyy") #'
            }
         ],
         groupable: true
     });

### `navigatable` : **Boolean** *(default: false)*

 Indicates whether keyboard navigation is enabled/disabled.

#### Example

    $("#grid").kendoGrid({
         dataSource: {
             data: createRandomData(50),
             pageSize: 10
         },
         columns: [
             {
                 field: "Name"
             },
             {
                 field: "BirthDate",
                 title: "Birth Date",
                 template: '#= kendo.toString(BirthDate,"dd MMMM yyyy") #'
            }
         ],
         navigatable: true
     });

### `pageable` : **Boolean** *(default: false)*

 Indicates whether paging is enabled/disabled.

#### Example

    $("#grid").kendoGrid({
         dataSource: {
             data: createRandomData(50),
             pageSize: 10
         },
         columns: [
             {
                 field: "Name"
             },
             {
                 field: "BirthDate",
                 title: "Birth Date",
                 template: '#= kendo.toString(BirthDate,"dd MMMM yyyy") #'
            }
         ],
         pageable: true
     });

### `rowTemplate` : **Function** 

Template to be used for rendering the rows in the grid.

#### Example

    //template
     <script id="rowTemplate" type="text/x-kendo-tmpl">
         <tr>
             <td>
                 <img src="${ BoxArt.SmallUrl }" alt="${ Name }" />
             </td>
             <td>
                 ${ Name }
             </td>
             <td>
                 ${ AverageRating }
             </td>
         </tr>
     </script>
    
     //grid intialization
     <script>PO details informaiton
         $("#grid").kendoGrid({
             dataSource: dataSource,
             rowTemplate: kendo.template($("#rowTemplate").html()),
             height: 200
         });
     </script>

### `scrollable` : **Boolean | Object** *(default: true)*

 Enable/disable grid scrolling. Possible values:
<div class="details-list">
   <dl>
        <dt>
             **true**
        </dt>
        <dd>
             Enables grid vertical scrolling
        </dd>
        <dt>
             **false**
        </dt>
        <dd>
             Disables grid vertical scrolling
        </dd>
        <dt>
             **{ virtual: false }**
        </dt>
        <dd>
             Enables grid vertical scrolling without data virtualization. Same as first option.
        </dd>
        <dt>
             **{ virtual: true }**
        </dt>
        <dd>
             Enables grid vertical scrolling with data virtualization.
        </dd>
   </dl>
</div>

#### Example

    $("#grid").kendoGrid({
         scrollable: {
             virtual: true //false
         }
     });

### `selectable` : **String** *(default: undefined)*

 Indicates whether selection is enabled/disabled. Possible values:
<div class="details-list">
   <dl>
        <dt>
             **"row"**
        </dt>
        <dd>
             Single row selection.
        </dd>
        <dt>
             **"cell"**
        </dt>
        <dd>
             Single cell selection.
        </dd>
        <dt>
             **"multiple, row"**
        </dt>
        <dd>
             Multiple row selection.
        </dd>
        <dt>
             **"multiple, cell"**
        </dt>
        <dd>
             Multiple cell selection.
        </dd>
   </dl>
</div>

### `sortable` : **Object** 

Defines whether grid columns are sortable.

#### Example

    $("#grid").kendoGrid({
        sortable: true
    });
    //
    // or
    //
    $("#grid").kendoGrid({
        sortable: {
            mode: "multiple", // enables multi-column sorting
            allowUnsort: true
    });

### `sortable.allowUnsort` : **Boolean** *(default: false)*

  Defines whether column can have unsorted state.

### `sortable.mode` : **String** *(default: "single")*

 Defines sorting mode. Possible values:
<div class="details-list">
   <dl>
        <dt>
             **"single"**
        </dt>
        <dd>
            Defines that only once column can be sorted at a time.
        </dd>
        <dt>
             **"multiple"**
        </dt>
        <dd>
             Defines that multiple columns can be sorted at a time.
        </dd>
   </dl>
</div>

### `toolbar` : **Array** 

This is a list of commands for which the corresponding buttons will be rendered.
The supported built-in commands are: "create", "cancel", "save", "destroy".

#### Example

    $("#grid").kendoGrid({
         dataSource: {
             data: createRandomData(50),
             pageSize: 10
         },
         columns: [
             {
                 field: "Name"
             },
             {
                 field: "BirthDate",
                 title: "Birth Date",
                 template: '#= kendo.toString(BirthDate,"dd MMMM yyyy") #'
            }
         ]
         toolbar: [
             "create",
             { name: "save", text: "Save This Record" },
             { name: "cancel", template: '<img src="icons/cancel.png' rel='cancel' />" }
         ],
         editable: true
      });

### `toolbar.name` : **String** 

The name of the command. One of the predefined or a custom.

### `toolbar.template` : **String** 

The template for the command button.

### `toolbar.text` : **String** 

The text of the command that will be set on the button.

## Methods

### addRow

Adds a new empty table row in edit mode. The addRow method triggers edit event.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    grid.addRow();

### cancelChanges

Cancels any pending changes during. Deleted rows are restored. Inserted rows are removed. Updated rows are restored to their original values.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    grid.cancelChanges();

### cancelRow

Switch the current edited row into display mode and revert changes made to the data

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    grid.cancelRow();

### cellIndex

Returns the index of the cell in the grid item skipping group and hierarchy cells.

#### Example

     // get a reference to the grid widget
     var grid = $("#grid").data("kendoGrid");
     // get the index of the row
     // TODO: add specific function call here

#### Parameters

##### cell `Selector | DOM Element`

Target cell.

### clearSelection

Clears currently selected items.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // clear the selection of items in the grid
    grid.clearSelection();

### closeCell

Closes current edited cell.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // close the cell being edited
    grid.closeCell();

### collapseGroup

Collapses specified group.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // collapses first group item
    grid.collapseGroup(grid.tbody.find(">tr.k-grouping-row:first"));

#### Parameters

##### group `Selector | DOM Element`

Target group item to collapse.

### collapseRow

Collapses specified master row.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // collapses first master row
    grid.collapseRow(grid.tbody.find(">tr.k-master-row:first"));

#### Parameters

##### row `Selector | DOM Element`

Target master row to collapse.

### dataItem

Returns the data item to which a given table row (tr DOM element) is bound.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // returns the data item for first row
    grid.dataItem(grid.tbody.find(">tr:first"));

#### Parameters

##### tr `Selector | DOM Element`

Target row.

### editCell

Puts the specified table cell in edit mode. It requires a jQuery object representing the cell. The editCell method triggers edit event.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // edit first table cell
    grid.editCell(grid.tbody.find(">tr>td:first"));

#### Parameters

##### cell `Selector`

Cell to be edited.

### editRow

Switches the specified row from the grid into edit mode. The editRow method triggers edit event.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // edit first table row
    grid.editRow(grid.tbody.find(">tr:first"));

#### Parameters

##### row `Selector | DOM Element`

Row to be edited.

### expandGroup

Expands specified group.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // expands first group item
    grid.expandGroup(grid.tbody.find(">tr.k-grouping-row:first"));

#### Parameters

##### group `Selector | DOM Element`

Target group item to expand.

### expandRow

Expands specified master row.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // expands first master row
    grid.expandRow(grid.tbody.find(">tr.k-master-row:first"));

#### Parameters

##### row `Selector | DOM Element`

Target master row to expand.

### refresh

Repaints the grid.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // refreshes the grid
    grid.refresh();

#### Parameters

##### e ``



### removeRow

Removes the specified row from the grid. The removeRow method triggers remove event.
(Note: In inline or popup edit modes the changes will be automatically synced)

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // remove first table row
    grid.removeRow(grid.tbody.find(">tr:first"));

#### Parameters

##### row `Selector | DOM Element`

Row to be removed.

### saveChanges

Calls DataSource sync to submit any pending changes if state is valid. The saveChanges method triggers saveChanges event.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    grid.saveChanges();

### saveRow

Switch the current edited row into dislay mode and save changes made to the data
(Note: the changes will be automatically synced)

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    grid.saveRow();

### select

Selects the specified Grid rows/cells. If called without arguments - returns the selected rows/cells.

#### Example

    // get a reference to the grid widget
    var grid = $("#grid").data("kendoGrid");
    // selects first grid item
    grid.select(grid.tbody.find(">tr:first"));

#### Parameters

##### items `Selector | Array`

Items to select.

## Events

### change

Fires when the grid selection has changed.

#### Example

     $("#grid").kendoGrid({
         change: function(e) {
             // handle event
         }
     });

#### To set after initialization

     // get a reference to the grid
     var grid = $("#grid").data("kendoGrid");
     // bind to the change event
     grid.bind("change", function(e) {
         // handle event
     }

### dataBound

Fires when the grid has received data from the data source.

#### Example

     $("#grid").kendoGrid({
         dataBound: function(e) {
             // handle event
         }
     });

#### To set after initialization

     // get a reference to the grid
     var grid = $("#grid").data("kendoGrid");
     // bind to the dataBound event
     grid.bind("dataBound", function(e) {
         // handle event
     }

### detailCollapse

Fires when the grid detail row is collapsed.

#### Example

     $("#grid").kendoGrid({
         detailCollapse: function(e) {
             // handle event
         }
     });

#### To set after initialization

     // get a reference to the grid
     var grid = $("#grid").data("kendoGrid");
     // bind to the detailCollapse event
     grid.bind("detailCollapse", function(e) {
         // handle event
     }

#### Event Data

##### e.masterRow `Object`

The jQuery element representing master row.

##### e.detailRow `Object`

The jQuery element representing detail row.

### detailExpand

Fires when the grid detail row is expanded.

#### Example

     $("#grid").kendoGrid({
         detailExpand: function(e) {
             // handle event
         }
     });

#### To set after initialization

     // get a reference to the grid
     var grid = $("#grid").data("kendoGrid");
     // bind to the detailExpand event
     grid.bind("detailExpand", function(e) {
         // handle event
     }

#### Event Data

##### e.masterRow `Object`

The jQuery element representing master row.

##### e.detailRow `Object`

The jQuery element representing detail row.

### detailInit

Fires when the grid detail is initialized.

#### Example

     $("#grid").kendoGrid({
         detailInit: function(e) {
             // handle event
     });

#### To set after initialization

     // get a reference to the grid
     var grid = $("#grid").data("kendoGrid");
     // bind to the detailInit event
     grid.bind("detailInit", function(e) {
         // handle event
     }

#### Event Data

##### e.masterRow `Object`

The jQuery element representing master row.

##### e.detailRow `Object`

The jQuery element representing detail row.

##### e.detailCell `Object`

The jQuery element representing detail cell.

##### e.data `Object`

The data for the master row.

### edit

Fires when the grid enters edit mode.

#### Example

     $("#grid").kendoGrid({
         edit: function(e) {
             // handle event
     });

#### To set after initialization

     // get a reference to the grid
     var grid = $("#grid").data("kendoGrid");
     // bind to the edit event
     grid.bind("edit", function(e) {
         // handle event
     }

#### Event Data

##### e.container `Object`

The jQuery element to be edited.

##### e.model `Object`

The model to be edited.

### remove

Fires before the grid item is removed.

#### Example

     $("#grid").kendoGrid({
         remove: function(e) {
             // handle event
     });

#### To set after initialization

     // get a reference to the grid
     var grid = $("#grid").data("kendoGrid");
     // bind to the remove event
     grid.bind("remove", function(e) {
         // handle event
     }

#### Event Data

##### e.row `Object`

The row element to be deleted.

##### e.model `Object`

The model which to be deleted.

### save

Fires before the grid item is changed.

#### Example

     $("#grid").kendoGrid({
         save: function(e) {
             // handle event
     });

#### To set after initialization

     // get a reference to the grid
     var grid = $("#grid").data("kendoGrid");
     // bind to the save event
     grid.bind("save", function(e) {
         // handle event
     }

#### Event Data

##### e.values `Object`

The values entered by the user.

##### e.container `Object`

The jQuery element which is in edit mode.

##### e.model `Object`

The edited model.

### saveChanges

Fires before the grid calls DataSource sync.

#### Example

     $("#grid").kendoGrid({
         saveChanges: function(e) {
             // handle event
     });

#### To set after initialization

     // get a reference to the grid
     var grid = $("#grid").data("kendoGrid");
     // bind to the saveChanges event
     grid.bind("saveChanges", function(e) {
         // handle event
     }