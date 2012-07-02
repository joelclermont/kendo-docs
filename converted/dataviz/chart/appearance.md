---
title: Appearance
publish: true
---

## 

## Chart Appearance 

The appearance of the Chart is controlled with style options.

This is in contrast with the other components in the suite that use CSS for styling.

### Chart structure

The main building blocks of the chart are:

*   Title
*   Legend
*   Chart Area
*   Plot Area
*   Axes
*   Series 

![Chart Structure](/Libraries/Documentation/chart-structure.sflb.ashx)

### Title

The title location can be controlled with the "position" property of the "title" object. Available options are:

*   top
*   bottom 

### Legend

The legend position is also controllable. Supported "position" values:

*   top
*   bottom
*   left
*   right
*   custom 

Custom positioning is configured through the "offsetX"&nbsp; and "offsetY" properties. For example:

![Custom legend position](/Libraries/Documentation/chart-legend-custom-position.sflb.ashx) 

Series can be excluded from the legend by setting their "visibleInLegend" property to "false".

### Themes

The Chart comes with a number of predefined themes:

*   Default
*   Black
*   BlueOpal
*   Metro
*   Silver 

Use the **theme** property to select a theme:

 
    $("#chart").kendoChart({
    theme: "blueOpal",
    series: [{
        type: "bar",
        name: "United States",
        data: [67.96, 68.93, 75, 74, 78]
    }],
    categoryAxis: {
        categories: [2005, 2006, 2007, 2008, 2009]
    }
    });
     

Note that theme names are case insensitive.

### Transitions

The Chart uses animated transitions to display new and updated data. These transitions can be disabled through the **transitions** property:
 
    $("#chart").kendoChart({
    series: [{
        type: "bar",
        name: "United States",
        data: [67.96, 68.93, 75, 74, 78]
    }],
    categoryAxis: {
        categories: [2005, 2006, 2007, 2008, 2009]
    },
    transitions: false
    });
     

### See also

Refer to the [Configuration section](http://www.kendoui.com/documentation/dataviz/chart/configuration.aspx) for a full list of configuration options for each element.