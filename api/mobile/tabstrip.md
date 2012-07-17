---
title: kendo.mobile.ui.TabStrip
slug: mobile-kendo.mobile.ui.tabstrip
tags: api,mobile
publish: true
---

# kendo.mobile.ui.TabStrip

## Configuration

### selectedIndex `Number`*(default: 0)*

 The index of the initially selected tab.

## Methods

### currentItem

Get the currently selected tab DOM element.

#### Returns

`jQuery` the currently selected tab DOM element.

### switchTo

Set the mobile TabStrip active tab to the tab with the specified url.

#### Example

    <div data-role="tabstrip" id="tabstrip"> <a href="#foo">Foo</a> </div>

    <script>
        $(function() {
            $("#tabstrip").data("kendoMobileTabStrip").switchTo("#foo");
        });
    </script>

#### Parameters

##### url `String`

The url of the tab.

## Events

### select

Fires when tab is selected.

#### Event Data

##### e.item `jQuery`

The selected tab
