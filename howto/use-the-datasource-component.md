---
title: Use the DataSource
slug: howto-use-the-datasource
tags: How-To
publish: true
---

# How-To: Use the DataSource

In this how-to, we'll examine how to use the DataSource of Kendo UI.

## Introduction

The DataSource plays a central role in the applications and sites built with Kendo UI. Fundamentally, it is an abstraction over local or remote data. However, it has many other responsibilities as well, including:

* retrieving data from a remote endpoint;
* maintaining the structure and type of the data it represents (schema);
* processing serialization formats to/from a remote endpoint;
* synchronizing updates (i.e. create, update, delete) to/from a remote endpoint;
* maintaining an in-memory cache of data (including changes) for a batch update to a remote endpoint;
* calculating and maintaining aggregates, sorting order, and page sizes;
* and, providing a query mechanism via filter expressions.

> To learn more about the capabilities of the DataSource, make sure to check out its [API reference](http://docs.kendoui.com/api/framework/datasource) or [demos](http://demos.kendoui.com/web/datasource/index.html).

## Creating a Local DataSource

Creating a DataSource to local data is simple:

	var movies = [
		{ title: "Star Wars: A New Hope", year: 1977 },
		{ title: "Star Wars: The Empire Strikes Back", year: 1980 },
		{ title: "Star Wars: Return of the Jedi", year: 1983 }
	];

	var localDataSource = new kendo.data.DataSource({ data: movies });

In this example, the variable, `localDataSource` is a DataSource that is initialized to represent an in-memory cache of the `movies` array. However, the data represented by the `movies` array is not loaded in the DataSource until the `.read()` method is called:

	localDataSource.read();

