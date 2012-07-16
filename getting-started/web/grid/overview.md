---
title: Grid Overview
slug: getting-started.web.grid
tags: getting-started,web
publish: true
---

# Grid Overview

The Grid widget displays tabular data and offers rich support interacting with data,
including paging, sorting, grouping, and selection. Grid is a powerful widget with
many configuration options. It can be bound to local JSON data or to remote data
using the Kendo DataSource component.


## Getting Started

There are two primary ways to create a Kendo Grid:



1.  From an existing HTML table element, defining columns, rows, and data in HTML
2.  From an HTML div element, defining columns and rows with configuration, and binding to data

### Creating a **Grid** from existing HTML Table element

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

### Initialize the Kendo Grid

      $(document).ready(function(){
          $("#grid").kendoGrid();
      });

### Creating a **Grid** from existing HTML Div element

     <!-- Define the HTML div that will hold the Grid -->
     <div id="grid">
     </div>

### Initialize the Kendo Grid and configure columns & data binding

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

## Configuring Grid Behavior

Kendo Grid supports paging, sorting, grouping, and scrolling. Configuring any of
these Grid behaviors is done using simple boolean configuration options. For
example, the follow snippet shows how to enable all of these behaviors.

### Enabling Grid paging, sorting, grouping, and scrolling

       $(document).ready(function(){
          $("#grid").kendoGrid({
             groupable: true,
             scrollable: true,
             sortable: true,
             pageable: true
          });
      });

By default, paging, grouping, and sorting are **disabled**. Scrolling is enabled by default.



## Performance with Virtual Scrolling

When binding to large data sets or when using large page sizes, reducing active in-memory
DOM objects is important for performance. Kendo Grid provides built-in UI virtualization
for highly optimized binding to large data sets. Enabling UI virtualization is done via simple configuration.

### Enabling Grid UI virtualization

       $(document).ready(function(){
          $("#grid").kendoGrid({
             scrollable: {
                 virtual: true
             }
          });
      });

## Accessing an Existing Grid

You can reference an existing **Grid** instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [Grid API](/api/web/grid) to control its behavior.

### Accessing an existing Grid instance

    var grid = $("#grid").data("kendoGrid");

