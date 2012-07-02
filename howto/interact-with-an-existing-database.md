---
title: How-To: Interact With An Existing Database
tags: How-To
publish: true
related:
---

# How-To: Interact With An Existing Database

In this how-to, we'll examine how to interact to an existing database.

## Introduction

[Introduction]

## DataSource

The DataSource component is an abstraction in JavaScript that manages in-memory and remote data sources. Its purpose is to simplify the process of propagating updates to and from these data sources. In the case where data stored in a remote database (SQL Server, Oracle, MySQL, CouchDB, etc.), it is already assumed that the data is accessible to query via HTTP. This is necessary since we are talking about JavaScript running in the context of the browser. So, at a basic level, this is what is required for us to integrate your data with our framework. In terms of the actual data coming across the wire, this can be represented in a number of different ways. Out-of-the-box, Kendo UI supports XML, OData, and JSON.

## Example: SQL Server

[Schema]
[Server Configuration]