---
title: DataSource Overview
slug: datasource-overview
publish: true
---

# Kendo DataSource Overview

The DataSource component is an abstraction for using local (arrays of JavaScript objects) or
remote (XML, JSON, JSONP) data. It fully supports CRUD (Create, Read, Update, Destroy) data
operations and provides both local and server-side support for sorting, paging, filtering, grouping, and aggregates.


## Getting Started

### Creating a DataSource bound to local data

    var movies = [ {
          title: "Star Wars: A New Hope",
          year: 1977
       }, {
         title: "Star Wars: The Empire Strikes Back",
         year: 1980
       }, {
         title: "Star Wars: Return of the Jedi",
         year: 1983
       }
    ];
    var localDataSource = new kendo.data.DataSource({data: movies});

### Creating a DataSource bound to a remote data service (Twitter)

    var dataSource = new kendo.data.DataSource({
        transport: {
            read: {
                // the remote service url
                url: "http://search.twitter.com/search.json",
    
                // JSONP is required for cross-domain AJAX
                dataType: "jsonp",
    
                // additional parameters sent to the remote service
                data: {
                    q: "html5"
                }
            }
        },
        // describe the result format
        schema: {
            // the data which the data source will be bound to is in the "results" field
            data: "results"
        }
    });

## Binding UI widgets to DataSource


Many Kendo UI widgets support data binding, and the Kendo UI DataSource is an ideal
binding source for both local and remote data. A DataSource can be created in-line
with other UI widget configuration settings, or a shared DataSource can be created
to enable multiple UI widgets to bind to the same, observable data collection.

### Creating a local DataSource in-line with UI widget configuration

    $("#chart").kendoChart({
        title: {
            text: "Employee Sales"
        },
        dataSource: new kendo.data.DataSource({
            data: [
            {
                employee: "Joe Smith",
                sales: 2000
            },
            {
                employee: "Jane Smith",
                sales: 2250
            },
            {
                employee: "Will Roberts",
                sales: 1550
            }]
        }),
        series: [{
            type: "line",
            field: "sales",
            name: "Sales in Units"
        }],
        categoryAxis: {
            field: "employee"
        }
    });

### Creating and binding to a sharable remote DataSource

    var sharableDataSource = new kendo.data.DataSource({
        transport: {
            read: {
                url: "data-service.json",
                dataType: "json"
            }
        }
    });
    
    // Bind two UI widgets to same DataSource
    $("#chart").kendoChart({
        title: {
            text: "Employee Sales"
        },
        dataSource: sharableDataSource,
        series: [{
            field: "sales",
            name: "Sales in Units"
        }],
        categoryAxis: {
            field: "employee"
        }
    });
    
    $("#grid").kendoGrid({
        dataSource: sharableDataSource,
            columns: [
            {
                field: "employee",
                title: "Employee"
            },
            {
                field: "sales",
                title: "Sales",
                template: '#= kendo.toString(sales, "N0") #'
        }]
    });
