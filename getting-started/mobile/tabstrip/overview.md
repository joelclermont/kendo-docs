---
title: Mobile TabStrip overview
slug: gs-mobile-tabstrip
tags: getting-started,mobile
publish: true
---

# Mobile TabStrip Overview

The mobile TabStrip widget is used inside a mobile view or layout footer element to display an application-wide group of navigation buttons.
The look of the mobile TabStrip changes depending on the user mobile device and operating system.

## Getting Started

The Kendo mobile Application will automatically initialize the mobile TabStrip for every element with `role` data attribute set to `tabstrip` present in the views/layouts markup.
Alternatively, it can be initialized using jQuery plugin syntax in the mobile View/Layout init event handler. The tabstrip element should contain one or more `a` elements.

## Kendo Mobile Application Integration

The tabs of the TabStrip navigate to the mobile application's views. When the mobile application navigates to another view, it updates the TabStrip's currently selected tab, based on the current view's URL.

### Initialize Kendo mobile TabStrip based on role data attribute.

    <div data-role="tabstrip">
        <a href="#index">Home</a>
        <a href="#featured">Featured</a>
    </div>

## Tab icons

A tab icon can be set in two ways - either by adding an `img` element inside the `a` element, or by setting an `icon` data attribute to the `a` element.
Kendo mobile TabStrip ships with several ready to use icons:

*   <span class="km-icon km-about"></span>about
*   <span class="km-icon km-action"></span>action
*   <span class="km-icon km-add"></span>add
*   <span class="km-icon km-bookmarks"></span>bookmarks
*   <span class="km-icon km-camera"></span>camera
*   <span class="km-icon km-cart"></span>cart
*   <span class="km-icon km-compose"></span>compose
*   <span class="km-icon km-contacts"></span>contacts
*   <span class="km-icon km-details"></span>details
*   <span class="km-icon km-downloads"></span>downloads
*   <span class="km-icon km-fastforward"></span>fastforward
*   <span class="km-icon km-favorites"></span>favorites
*   <span class="km-icon km-featured"></span>featured
*   <span class="km-icon km-toprated"></span>toprated
*   <span class="km-icon km-globe"></span>globe
*   <span class="km-icon km-history"></span>history
*   <span class="km-icon km-home"></span>home
*   <span class="km-icon km-info"></span>info
*   <span class="km-icon km-more"></span>more
*   <span class="km-icon km-mostrecent"></span>mostrecent
*   <span class="km-icon km-mostviewed"></span>mostviewed
*   <span class="km-icon km-organize"></span>organize
*   <span class="km-icon km-pause"></span>pause
*   <span class="km-icon km-play"></span>play
*   <span class="km-icon km-recents"></span>recents
*   <span class="km-icon km-refresh"></span>refresh
*   <span class="km-icon km-reply"></span>reply
*   <span class="km-icon km-rewind"></span>rewind
*   <span class="km-icon km-search"></span>search
*   <span class="km-icon km-settings"></span>settings
*   <span class="km-icon km-share"></span>share
*   <span class="km-icon km-stop"></span>stop
*   <span class="km-icon km-trash"></span>trash

Additional icons may be added by defining the respective CSS tab class.

## Creating Custom Icons

In order to create colorizable icons like the default ones in Kendo UI Mobile, specify the icon image as a **box mask**
(either as dataURI or as a separate image). The image should be **PNG8** or **PNG24** with alpha channel (**PNG8+Alpha** is supported by
only few graphic editors, so **better stick with PNG24**). The image color is not important - it will be used as a mask only.

**Note**: **BlackBerry 7.0** has a bug that renders its masks as background-image, so it is recommended to use white in order to support it. The bug is fixed in **7.1**.

### Define custom tab icon

    <style>
    .km-custom {
      -webkit-mask-box-image: url("foo.png");
    }
    </style>

    <div data-role="tabstrip">
      <a href="#index" data-icon="custom">Home</a>
    </div>

