---
title: Interact With an Existing DB
slug: howto-interact-with-an-existing-db
tags: How-To
publish: true
---

# How-To: Interact With An Existing Database

In this how-to, we'll examine how to interact with an existing database via the DataSource of Kendo UI.

## Introduction to the DataSource

The DataSource plays a central role in the applications and sites built with Kendo UI. Fundamentally, it is an abstraction over local or remote data. However, it has many other responsibilities as well, including:

* retrieving data from a remote endpoint;
* maintaining the structure and type of the data it represents (schema);
* processing serialization formats to/from a remote endpoint;
* synchronizing updates (i.e. create, update, delete) to/from a remote endpoint;
* maintaining an in-memory cache of data (including changes) for a batch update to a remote endpoint;
* calculating and maintaining aggregates, sorting order, and page sizes;
* and, providing a query mechanism via filter expressions.

> To learn more about the capabilities of the DataSource, make sure to check out its [API reference](http://docs.kendoui.com/api/framework/datasource) or [demos](http://demos.kendoui.com/web/datasource/index.html).

## Exposing Data via HTTP(S)

Many modern databases support the ability to expose data via Internet-friendly protocols like HTTP(S). However, it is strongly recommended to implement a service layer to expose this data instead. Doing so will provide a number of benefits to the producers and consumers of this data. These benefits include:

* improved useability through APIs and (optionally) denormalization;
* reduced exposure of (potentially) sensitive data;
* and/or, abstraction layer for additional architectural concerns (i.e. service throttling).

There are many frameworks that support the creation of service endpoints like [ASP.NET Web API](http://www.asp.net/web-api).

## Accessing Remote Data

The DataSource may query a remote endpoint that provides data stored in a remote database (SQL Server, Oracle, MySQL, CouchDB, etc.) via HTTP(S). Operations conducted by the DataSource against this remote endpoint are done so via [jQuery.ajax()](http://api.jquery.com/jQuery.ajax/) and therefore, subject to the same security constraints enforced by the user agent. Additional security constraints also apply to XHRs made across different domains. The DataSource may query remote endpoints from different domains via [JSONP](http://en.wikipedia.org/wiki/JSONP). This is accomplished by setting the `dataType` configuration property:

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

In this example, the DataSource is initialized to represent an in-memory cache of tweets from the search service for Twitter. Setting the `dataType` configuration property is required to instruct the DataSource to access the endpoint.

> Refer to the how-to article entitled, [How To: Use CORS with All (Modern) Browsers](http://docs.kendoui.com/howto/use-cors-with-all-modern-browsers) for more information about Cross-Origin Resource Sharing (CORS).