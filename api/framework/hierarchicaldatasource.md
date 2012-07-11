---
title: kendo.data.HierarchicalDataSource
slug: fw-kendo.data.hierachicaldatasource
tags: api,framework
publish: true
---

# kendo.data.HierarchicalDataSource

## Description

The HierarchicalDataSource component extends the [DataSource component](/api/framework/datasource), allowing
representation of hierarchical data. This help topic assumes that you are familiar with the
Kendo UI DataSource, and builds upon that knowledge with information that is specific to
hierarchical data.

### Getting Started

#### Creating a HierarchicalDataSource bound to local data

    var categorizedMovies = [ {
          categoryName: "SciFi",
          items: [
            { title: "Star Wars: A New Hope", year: 1977 },
            { title: "Star Wars: The Empire Strikes Back", year: 1980 },
            { title: "Star Wars: Return of the Jedi", year: 1983 }
          ]
      }, {
          categoryName: "Drama",
          items: [
            { title: "The Shawshenk Redemption", year: 1994 },
            { title: "Fight Club", year: 1999 },
            { title: "The Usual Suspects", year: 1995 }
          ]
      }
    ];
    var localDataSource = new kendo.data.HierarchicalDataSource({ data: categorizedMovies });

#### Creating a HierarchicalDataSource bound to a homogeneous remote data service

    var homogeneous = new kendo.data.HierarchicalDataSource({
        transport: {
            read: {
                url: "http://demos.kendoui.com/service/Employees",
                dataType: "json"
            }
        },
        schema: {
            model: {
                id: "EmployeeId",
                hasChildren: "HasEmployees"
            }
        }
    });

The above snippet will target the HierarchicalDataSource to a single service end-point.
The data service is homogeneous, i.e. it always returns objects of the same type.
After executing `homogeneous.read()`, the service end-point is hit without a EmployeeId parameter:

    GET http://demos.kendoui.com/service/Employees

    => [ { "EmployeeId": 2, "Name": "Andrew", "HasEmployees": true } ]

Reading the children of the returned item is achieved by calling the `load` method of the data item:

    var ceo = homogeneous.view()[0];

    ceo.load();

This will hit the service end-point and will supply the id of the data item:

    GET http://demos.kendoui.com/service/Employees?EmployeeId=2

    => [
          { "EmployeeId": 3, "Name": "Bob", "HasEmployees": false },
          { "EmployeeId": 4, "Name": "Charlie", "HasEmployees": false }
       ]

Now, the children can be accessed:

    // ceo.children is a HierarchicalDataSource, too
    var middleManagement = ceo.children.view();


#### Binding a HierarchicalDataSource to remote data with multiple service end-points

    // configuration of the products service end-point
    var Products = {
            transport: {
                read: {
                    url: "http://demos.kendoui.com/service/Products",
                    dataType: "json"
                }
            },
            schema: {
                data: "products",
                model: {
                    hasChildren: false
                }
            }
        };

    // configuration of the categories service end-point
    var Categories = new kendo.data.HierarchicalDataSource({
        transport: {
            read: {
                url: "http://demos.kendoui.com/service/Categories",
                dataType: "json"
            }
        },
        schema: {
            data: "categories",
            model: {
                id: "categoryId",

                // categories will always have children
                hasChildren: true,

                // children will be fetched from the Products end-point
                children: Products
            }
        }
    });

The configuration above creates a two-level HierarchicalDataSource (categories and products) that
fetches data from two different end-points (/service/Categories and /service/Products, respectively).

### Binding UI widgets to HierarchicalDataSource

At this time, the only widget that is aware of the HierarchicalDataSource is the TreeView.


## Configuration

See the [DataSource configuration](/api/framework/datasource#configuration) for all inherited configuration.

### schema.model.hasChildren `Boolean | String | Function`

### schema.model.children `Object`

## Methods

See the [DataSource methods](/api/framework/datasource#methods) for all inherited methods.

The **remove** and **getByUid** methods are overridden and work with the hierarchical data
(they will act on all child datasources that have been read).
