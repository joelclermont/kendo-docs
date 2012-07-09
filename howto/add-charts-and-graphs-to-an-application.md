---
title: Add Charts and Graphs
slug: howto-add-charts-and-graphs
tags: How-To
publish: true
---

# How-To: Add Charts and Graphs with Kendo UI DataViz

In this how-to, we'll examine how to add charts and graphs to an application with [Kendo UI DataViz](http://kendoui.com/dataviz.aspx).

Let's begin by examining how to add an area chart to an existing page. For this example, let's assume the following HTML for this page:

	<!DOCTYPE html>
	<html lang="en">
	<head>
		<meta charset="utf-8">
		<title>My Kendo UI Application</title>
	</head>
	<body>
		<header>
			<h1>My Kendo UI Application</h1>
		</header>
		<div role="main">

		</div>
		<footer>
			<p>Kendo UI FTW!</p>
		</footer>
	</body>
	</html>

The first step is to add the necessary script and stylesheet references for Kendo UI:

	<!DOCTYPE html>
	<html lang="en">
	<head>
		<meta charset="utf-8">
		<title>My Kendo UI Application</title>

		<!-- contains a small number of CSS rules and classes for styling charts and gauges -->
		<link rel="stylesheet" href="//cdn.kendostatic.com/2012.2.621/styles/kendo.dataviz.min.css">

	</head>
	<body>
		<header>
			<h1>My Kendo UI Application</h1>
		</header>
		<div role="main">
		</div>
		<footer>
			<p>Kendo UI FTW!</p>
		</footer>

		<!-- Google CDN reference for jQuery; utilizing a local reference if offline -->
		<script src="//ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
		<script>window.jQuery || document.write('<script src="js/jquery.min.js"><\/script>')</script>

		<!-- Kendo UI CDN reference for DataViz; utilizing a local reference if offline -->
		<script src="//cdn.kendostatic.com/2012.2.621/js/kendo.dataviz.min.js"></script>
		<script>(window.kendo && window.kendo.dataviz) || document.write('<script src="js/kendo.dataviz.min.js"><\/script>')</script>

	</body>
	</html>

> Please refer to the [JavaScript Dependencies of Kendo UI](http://docs.kendoui.com/getting-started/javascript-dependencies) for more information about script requirements for Kendo UI Web, Kendo UI DataViz, and Kendo UI Mobile.

The next step is to declare a target element for your data visualization. Typically, this is represented by a `div` element. A script block to initialize and configure the area chart is also required.

	<!DOCTYPE html>
	<html lang="en">
	<head>
		<meta charset="utf-8">
		<title>My Kendo UI Application</title>

		<!-- contains a small number of CSS rules and classes for styling charts and gauges -->
		<link rel="stylesheet" href="//cdn.kendostatic.com/2012.2.621/styles/kendo.dataviz.min.css">

	</head>
	<body>
		<header>
			<h1>My Kendo UI Application</h1>
		</header>
		<div role="main">
			<!-- chart/gauge -->
			<div id="chart">
			</div>
		</div>
		<footer>
			<p>Kendo UI FTW!</p>
		</footer>

		<!-- Google CDN reference for jQuery; utilizing a local reference if offline -->
		<script src="//ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
		<script>window.jQuery || document.write('<script src="js/jquery.min.js"><\/script>')</script>

		<!-- Kendo UI CDN reference for DataViz; utilizing a local reference if offline -->
		<script src="//cdn.kendostatic.com/2012.2.621/js/kendo.dataviz.min.js"></script>
		<script>(window.kendo && window.kendo.dataviz) || document.write('<script src="js/kendo.dataviz.min.js"><\/script>')</script>

		<script>
			// .ready() to initialise and configuration chart/gauge
			jQuery(document).ready(function($) {
				$("#chart").kendoChart({
					// configuration properties and settings go here
				});
			});
		</script>

	</body>
	</html>
