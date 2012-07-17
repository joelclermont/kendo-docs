---
title: AutoComplete Overview
slug: getting-started.web.autocomplete
tags: getting-started,web
publish: true
---

# AutoComplete Overview

The **AutoComplete** provides suggestions depending on the typed
text. It also allows multiple value entries. The suggestions shown by
the **AutoComplete** can come from a local Array or from a remote data service.


## Getting Started

### Create a HTML input element

    <input id="autoComplete" />

### Initialize the AutoComplete using a jQuery selector

    $(document).ready(function() {
     $("#autoComplete").kendoAutoComplete(["Item1", "Item2"]);
    });

## AutoComplete Suggestions


There are two primary ways to provide the **AutoComplete**
suggestions:


1.  From a local array
2.  From a remote data service



Locally defined values are best for small, fixed sets of suggestions.
Remote suggestions should be used for larger data sets. When used
with the **DataSource** component,
filtering large remote data services can be pushed to the server as
well, maximizing client-side performance.


## Local Suggestions


To configure and provide **AutoComplete** suggestions locally, you
can either pass an array directly to its constructor or you can set
the dataSource property to an local array.

### Directly initialize suggestions in constructor

    $("#autoComplete").kendoAutoComplete(["Item1", "Item2", "Item3"]);

### Using dataSource property to bind to local Array

    var data = ["Item1", "Item2", "Item3"];
    $("#autoComplete").kendoAutoComplete({
       dataSource: data
    });

## Remote Suggestions


The easiest way to bind an **AutoComplete** to remote
suggestions is to use the
**DataSource** component; an
abstraction for local and remote data. The **DataSource**
component can be used to serve data from a variety of data services,
such as
[XML](http://en.wikipedia.org/wiki/XML),
[JSON](http://en.wikipedia.org/wiki/JSON), and
[JSONP](http://en.wikipedia.org/wiki/JSONP).

### Using the Kendo UI Web DataSource component to bind to
remote suggestions with OData

    $(document).ready(function(){
     $("#autoComplete").kendoAutoComplete({
      minLength: 3,
      dataTextField: "Name", // JSON property name to use
      dataSource: new kendo.data.DataSource({
       type: "odata", // specifies data protocol
       pageSize: 10, // limits result set
       transport: {
        read: "http://odata.netflix.com/Catalog/Titles"
       }
      })
     })
    });

### Using the Kendo UI Web DataSource to bind to JSONP
suggestions

    $(document).ready(function(){
     $("#autoComplete").kendoAutoComplete({
      minLength:6,
      dataTextField:"title",
      filter: "contains",
      dataSource: new kendo.data.DataSource({
       transport: {
        read: {
         url: "http://api.geonames.org/wikipediaSearchJSON",
         data: {
          q: function(){
           return $("#autoComplete").data("kendoAutoComplete").value();
          },
          maxRows: 10,
          username: "demo"
         }
        }
       },
       schema: {
        data:"geonames"
       }
      }),
      change: function(){
       this.dataSource.read();
      }
     })
    });

## Accessing an Existing AutoComplete


You can reference an existing **AutoComplete** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the API to control
its behavior.

### Accessing an existing AutoComplete instance

    var autoComplete = $("#autoComplete").data("kendoAutoComplete");


