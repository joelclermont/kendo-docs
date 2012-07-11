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

## Creating a DataSource for Local Data

Creating a DataSource for local data is simple:

	var movies = [
		{ title: "Star Wars: A New Hope", year: 1977 },
		{ title: "Star Wars: The Empire Strikes Back", year: 1980 },
		{ title: "Star Wars: Return of the Jedi", year: 1983 }
	];

	var localDataSource = new kendo.data.DataSource({ data: movies });

In this example, the variable, `localDataSource` is a DataSource that is initialized to represent an in-memory cache of the `movies` array. However, the data represented by the `movies` array is not loaded in the DataSource until the `.read()` method is called:

	localDataSource.read();

When the DataSource is bound to a widget or chart, the explicit invocation may not be necessary; their default configuration is set to automatically bind to an associated DataSource. However, this may be overriden (i.e. `autoBind`).

## Creating a DataSource for Remote Data

The process of creating a DataSource for remote data differs in several ways from creating a DataSource for a local data:

* a transport must identify the protocol(s), URL(s) of endpoints, and serialization format(s) for any/all CRUD operations;
* optionally requires the use of a `parameterMap`, which marshalls request parameters to the format of a remote endpoint;
* and, optionally configures the use of server operations for calculating aggregates, defining filters, and supporting features like grouping, paging, and sorting.

Here's an example of creating a DataSource for data from a remote endpoint:

	var remoteDataSource = new kendo.data.DataSource({
		type: "odata",
		transport: {
			read: "http://odata.netflix.com/Catalog/Titles"
		}
	});

The variable, `remoteDataSource` is a DataSource that is initialized to represent an in-memory cache of movies titles from the Netflix catalog service, which employs the [OData](http://www.odata.org/). It is only configured to act as a read-only source of data to any widgets to which it is bound.

As is the case with creating a DataSource for local data, the data provided by the Netflix catalog service is not loaded until the `.read()` method is called:

	remoteDataSource.read();

When the DataSource is bound to a widget or chart, the explicit invocation may not be necessary; their default configuration is set to automatically bind to an associated DataSource. However, this may be overriden (i.e. `autoBind`).

Here's another example of creating a DataSource for data from a remote endpoint:

	var remoteDataSource = new kendo.data.DataSource({
		transport: {
			read: {
				url: "http://search.twitter.com/search.json",
				dataType: "jsonp",
				data: {
					q: function() {
						return $("#searchFor").val();
					}
				}
			}
		}
	});

In this example, the DataSource is initialized to represent an in-memory cache of tweets from the search service for Twitter. This endpoint employs a [JSON](http://www.json.org/)-based endpoint as denoted by the `dataType` configuration property. The endpoint contact specifies a parameter, `q` to denote a query string for the search service. Here, its value is provides by a input element on the page.