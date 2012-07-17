---
title: Mobile ButtonGroup overview
slug: gs-mobile-buttongroup
tags: getting-started,mobile
publish: true
---

# Mobile ButtonGroup Overview

The Kendo mobile ButtonGroup widget presents a linear set of grouped buttons.

## Getting Started

The Kendo mobile Application will automatically initialize a mobile ButtonGroup for every element with `role` data attribute set to `buttongroup`
present in the views/layouts markup. Alternatively, it can be initialized using jQuery plugin syntax in the containing mobile View **init event handler**. The ButtonGroup element should be `UL` element.

### Initialize Kendo mobile ButtonGroup based on role data attribute.

    <ul id="buttongroup" data-role="buttongroup">
        <li>Option 1</li>
        <li>Option 2</li>
    </ul>

### Initialize Kendo mobile ButtonGroup using jQuery plugin syntax

    var buttongroup = $("#buttongroup").kendoMobileButtonGroup();

## Customizing Mobile ButtonGroup Appearance


Every Kendo Mobile ButtonGroup color can be customized by setting the respective `background-color` CSS property inline or with a CSS selector.

### Green Kendo mobile ButtonGroup

    <ul id="buttongroup" data-role="buttongroup">
        <li style="background-color: green">Option1</li>
        <li style="beckground-color: red">Option2</li>
    </ul>

## Button Icons

A Button icon can be set in two ways - either by adding an `img` element inside the Button `a` element,
or by setting an `icon` data attribute to the Button `a` element.

KendoUI Mobile ships with several ready to use icons:

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



## Creating Custom Icons

In order to create colorizable icons like the default ones in Kendo UI Mobile, specify the icon image as a **box mask**
(either as dataURI or as a separate image). The image should be **PNG8** or **PNG24** with alpha channel (**PNG8+Alpha** is supported by
only few graphic editors, so **better stick with PNG24**). The image color is not important - it will be used as a mask only.

**Note**: **BlackBerry 7.0** has a bug that renders its masks as background-image, so it is recommended to use white in order to support it. The bug is fixed in **7.1**.

### Define custom button icon

    <style>
        .km-custom {
            -webkit-mask-box-image: url("foo.png");
        }
    </style>

    <ul id="buttongroup" data-role="buttongroup">
        <li data-icon="custom">Option 1</li>
        <li>Option 2</li>
    </ul>

