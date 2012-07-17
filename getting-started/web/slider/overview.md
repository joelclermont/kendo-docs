---
title: Slider Overview
slug: slider-overview
tags: getting-started,web
publish: true
---

# Slider Overview

The **Slider** provides a rich input for selecting values. Unlike the HTML5
range input, the **Slider** presents a consistent experience across browsers and features a rich
API and event model.

## Getting Started

### Create an input element

    <input id="slider" />

Initialization of a **Slider** should occur after the DOM is fully loaded. It is recommended that
initialization the **Slider** occur within a handler is provided to $(document).ready().

### Initialize a Slider using a selector within $(document).ready()

    $(document).ready(function() {
        $("#slider").kendoSlider();
    });

## Customizing Slider Behaviors

Many facets of the **Slider** behavior can be configured through
properties, including:

*   Minimum and/or maximum values
*   Orientation (horizontal or vertical)
*   Small or large step
*   Tooltip format/placement

### Initialize a Slider and its properties

    $("#slider").kendoSlider({
        min: 10,
        max: 50,
        orientation: "vertical",
        smallStep: 1,
        largeStep: 10
    });

## Accessing an Existing Slider

You can reference an existing **Slider** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

### Accessing an existing Slider instance

    var slider = $("#slider").data("kendoSlider");

