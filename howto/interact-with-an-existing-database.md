---
title: Interact With an Existing DB
slug: howto-interact-with-an-existing-db
tags: How-To
publish: true
---

# How-To: Interact With An Existing Database

In this how-to, we'll examine how to interact with an existing database via the DataSource component of Kendo UI.

The DataSource component plays a central role in the applications and sites built with Kendo UI. Fundamentally, it is an abstraction over local or remote data. However, it has many other responsibilities as well, including:

* retrieving data from a remote endpoint;
* maintaining the structure and type of the data it represents (schema);
* processing serialization formats to/from a remote endpoint;
* synchronizing updates (i.e. create, update, delete) to/from a remote endpoint;
* maintaining an in-memory cache of data (including changes) for a batch update to a remote endpoint;
* calculating and maintaining aggregates, sorting order, and page sizes;
* and, providing a query mechanism via filter expressions.

> To learn more, make sure to check out the [API reference](http://docs.kendoui.com/api/framework/datasource) or [demos](http://demos.kendoui.com/web/datasource/index.html) of the DataSource.

## Connecting the DataSource Component to a Remote Database

The DataSource component may only access remote data exposed via HTTP(S).

In the case where data stored in a remote database (SQL Server, Oracle, MySQL, CouchDB, etc.), it is already assumed that the data is accessible to query via HTTP. This is necessary since we are talking about JavaScript running in the context of the browser. So, at a basic level, this is what is required for us to integrate your data with our framework. In terms of the actual data coming across the wire, this can be represented in a number of different ways. Out-of-the-box, Kendo UI supports XML, OData, and JSON.