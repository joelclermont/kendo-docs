---
title: Add Charts and Graphs
slug: howto-add-charts-and-graphs
tags: How-To
publish: true
---

# How-To: Add Charts and Graphs to an Application

In this how-to, we'll examine how to add charts and graphs to an application with [Kendo UI DataViz](http://kendoui.com/dataviz.aspx).

## A Brief Introduction to Kendo UI DataViz

[Kendo UI DataViz](http://www.kendoui.com/dataviz.aspx) is a collection of [Kendo UI](http://www.kendoui.com/) that features a number of data visualizations that you can incorporate into your new and/or existing applications. These data visualizations include:

- Area Charts
- Bar Charts
- Bubble Charts
- Donut Charts
- Line Charts
- Pie Charts
- Scatter Charts
- Radial Gauges
- Linear Gauges

[Kendo UI DataViz](http://www.kendoui.com/dataviz.aspx) generates data visualizations through DOM elements on a page, much in a similar manner as widgets in [Kendo UI Web](http://www.kendoui.com/web.aspx).

### "Hello, DataViz!"

Let's begin by examining how to add a simple Area Chart to an existing page. For this example, let's assume the following HTML for this page:

	<!DOCTYPE html>
	<html>
	<head>
		<title>My Kendo UI Application</title>
	</head>
	<body>
		<h1>My Kendo UI Application</h1>
	</body>
	</html>

The first step is to add the necessary script and stylesheet references for Kendo UI, including a script reference to Kendo UI DataViz in order to utilize its data visualization widgets.

	<!DOCTYPE html>
	<html>
	<head>
		<title>My Kendo UI Application</title>
		<link href="styles/kendo.dataviz.min.css" rel="stylesheet" type="text/css" />
		<script src="js/jquery.min.js" type="text/javascript"></script>
		<script src="js/kendo.dataviz.min.js" type="text/javascript"></script>
	</head>
	<body>
		<h1>My Kendo UI Application</h1>
	</body>
	</html>

Note that a reference to jQuery has been included in the example (above) and it is the only external dependency for Kendo UI.

> Please refer to the [JavaScript Dependencies of Kendo UI](http://docs.kendoui.com/getting-started/javascript-dependencies) for more information about script requirements for Kendo UI Web, Kendo UI DataViz, and Kendo UI Mobile.

The next step is to declare a target element for your data visualization. Typically, this is represented by a `div` element.

	<!DOCTYPE html>
	<html>
	<head>
		<title>My Kendo UI Application</title>
		<link href="styles/kendo.dataviz.min.css" rel="stylesheet" type="text/css" />
		<script src="js/jquery.min.js" type="text/javascript"></script>
		<script src="js/kendo.dataviz.min.js" type="text/javascript"></script>
	</head>
	<body>
		<h1>My Kendo UI Application</h1>
		<div id="chart"></div>
	</body>
	</html>
