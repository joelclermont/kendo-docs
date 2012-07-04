---
title: Data Binding
slug: chart-data-binding
publish: true
---

# Data Binding

*   [Binding to inline data](#binding-to-inline-data)

    *   [Categorical series](#categorical-series)
    *   [Pie series](#pie-series)
    *   [Scatter series](#scatter-series)
    
*   [Binding to a Data Source](#binding-to-a-data-source)

    *   [Specifying a Data Source](#specifying-a-data-source)
    *   [Binding to local data](#binding-to-local-data)
    *   [Binding to remote data](#binding-to-remote-data)

*   [Data-bound Series](#data--bound-series)

    *   [Categorical series](#data--bound-categorical-series)
    *   [Pie series](#data--bound-pie-series)
    *   [Scatter series](#data--bound-scatter-series)

## Binding to inline data

The chart data points can be specified as part of the series definitions. The type of the data points depends on the type of the series.

### Categorical series

Categorical series such as bar, line, area, etc. expect a data point of type Number.

    $("#chart").kendoChart({
        series: [{
            name: "Example Series",
            type: "column",
            data: [200, 450, 300, 125]
       }]
    });


### Pie series

Series of type pie can also be bound to Number data points as above. These series also accept objects that fully describe each point:

    $("#chart").kendoChart({
        series: [{
            name: "Example Series",
            type: "pie",
            data:[{
                value: 40,
                category: "Apples"
            }, {
                value: 60,
                category: "Oranges",
                color: "#ff6103"
            }]
           }]
    });

### Scatter series

This category includes the two-dimensional scatter and scatter line series. The data point should be an array containing two values - X and Y.

    $("#chart").kendoChart({
        series:[{
            name: "Example Series",
            type: "scatterLine",
            data:[[1, 1], [1, 2]]
        }]
    });



## Binding to a Data Source

The DataSource component can be used to bind the Chart to both local and remote data. It supports variety of formats, including JSON, JSONP, XML, and OData.

### Specifying a Data Source

The Chart will accept either a DataSource instance or an object with the DataSource options.

For example:

    $("#chart").kendoChart({
        dataSource:{
            data: chartData
        }
    });


is the same as:

    var ds = new kendo.data.DataSource({
         data: chartData
    });

    $("#chart").kendoChart({
        dataSource: ds
    });

### Binding to local data

The chart can use existing objects as data points. For example, define the following array of objects.

    var seriesData = [ { year: "2000", sales: 200 },
               { year: "2001", sales: 450 },
               { year: "2002", sales: 300 },
               { year: "2003", sales: 125 } ];

    $("#chart").kendoChart({
        dataSource: {
            data: seriesData
        }
    });

### Binding to remote data

The chart can be bound to remote data by configuring the DataSource `transport`. The transport defines how the DataSource will interact with remote data.

In the below example, the following JSON string is returned from the "/sales" service.

    [ { "year": "2000", "sales": 200 },
      { "year": "2001", "sales": 450 },
      { "year": "2002", "sales": 300 },
      { "year": "2003", "sales": 125 }
    ]


We will bind the data source to this service and sort it by year.

    $("#chart").kendoChart({
        dataSource: {
            transport: {
                read: {
                    url: "/sales",
                    dataType: "json"
                }
            },
            sort: {
                field: "year",
                dir: "asc"
            }
        }
    });

## Data-bound Series

Some or all series can be bound to the data source items. The configuration is specific to the series type.

### Data-bound categorical series

Categorical series such as bar, line, area, etc. require a value "field". Categories are bound through the categoryAxis options.

    var seriesData = [ { year: "2000", sales: 200 } ];

    $("#chart").kendoChart({
        title: {
            text: "Kendo Chart Example"
        },
        dataSource: {
            data: seriesData
        },
        series: [{
            name: "Sales",
            field: "sales"
        }],
        categoryAxis: {
            field: "year"
        }
    });



### Data-bound pie series

In addition to the value "field", series of type pie accept fields for each point property - "categoryField", "colorField", etc.

    var seriesData = [ { year: "2000", sales: 200 } ];

    $("#chart").kendoChart({
        title: {
            text: "Kendo Chart Example"
        },
        dataSource: {
            data: seriesData
        },
        series: [{
            type: "pie",
            field: "sales",
            categoryField: "year"
        }]
    });

### Data-boiund scatter series

Scatter and scatter line series accept "xField" and "yField" options.

    var xyData = [ { x: 10, y: 20 } ];

    $("#chart").kendoChart({
        title: {
            text: "Kendo Chart Example"
        },
        dataSource: {
            data: xyData
        },
        series: [{
            name: "Plot",
            xField: "x",
            yField: "y"
        }]
    });

