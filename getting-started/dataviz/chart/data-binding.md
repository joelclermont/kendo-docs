---
title: Data Binding
slug: chart-data-binding
publish: true
---

## Data Binding

*   [Binding to inline data](#inline)
        *   [Categorical series](#inline-categorical)
    *   [Pie series](#inline-pie)
    *   [Scatter series](#inline-scatter)*   [Binding to a Data Source](#data-source)
        *   [Specifying a Data Source](#data-source-specifying)
    *   [Binding to local data](#data-source-local)
    *   [Binding to remote data](#data-source-remote)
    *   [Data-bound Series](#data-source-series)
            *   [Categorical series](#data-source-series-categorical)
        *   [Pie series](#data-source-series-pie)
        *   [Scatter series](#data-source-series-scatter) 

* * *
 <a name="inline"></a> 

## Binding to inline data

The chart data points can be specified as part of the series definitions. The type of the data points depends on the type of the series.
 <a name="inline-categorical"></a> 

### Categorical series

Categorical series such as bar, line, area, etc. expect a data point of type Number.
 
    $("#chart").kendoChart({
    series: [{
        name: "Example Series",
        type: "column",
        data: [200, 450, 300, 125]
       }]
    }); 
     

&nbsp;
 <a name="#inline-pie"></a> 

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

The full set of supported properties is available in the [Configuration section](http://www.kendoui.com/documentation/dataviz/chart/configuration.aspx).
 <a name="#inline-scatter"></a> 

### Scatter series 

This category includes the two-dimensional scatter and scatter line series. The data point should be an array containing two values - X and Y.
 
    $("#chart").kendoChart({
    series:[{
        name: "Example Series",
        type: "scatterLine",
        data:[[1, 1], [1, 2]]
    }]
    });
     

&nbsp;
 <a name="#data-source"></a> 

## Binding to a Data Source

The [DataSource component](http://www.kendoui.com/documentation/framework/datasource/overview.aspx) can be used to bind the Chart to both local and remote data. It supports variety of formats, including JSON, JSONP, XML, and OData.

&nbsp;
 <a name="#data-source-specifying"></a> 

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
    });&nbsp; <a name="#data-source-local"></a> 

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
     <a name="#data-source-remote"></a> 

### Binding to remote data

The chart can be bound to remote data by configuring the DataSource “_transport_”. The transport defines how the DataSource will interact with remote data.

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
     <a name="#data-source-series"></a> 

### Data-bound Series

Some or all series can be bound to the data source items. The configuration is specific to the series type.
 <a name="#data-source-series-categorical"></a> 

#### Categorical series

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
     

&nbsp;
 <a name="#data-source-series-pie"></a> 

#### Pie series

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
     <a name="#data-source-series-scatter"></a> 

#### Scatter series

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
     

&nbsp;

## 