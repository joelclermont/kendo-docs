---
title: Mobile Switch overview
slug: gs-mobile-switch
tags: getting-started,mobile
publish: true
---

# Mobile Switch Overview

The mobile Switch widget is used to display two exclusive choices.

When initialized, it shows the currently selected value. User slides the control to reveal the second value.
The mobile Switch can be created from `input` element of type `checkbox`.

## Getting Started

The Kendo Mobile Application will automatically initialize a mobile Switch for every element with `role` data attribute set to `swtich` present in the views/layouts markup.
Alternatively, it can be initialized using jQuery plugin syntax in the containing mobile View **init event handler**.

### Initialize mobile Switch based on role data attribute

    <input type="checkbox" data-role="switch" />

### Initialize mobile Switch using jQuery plugin syntax

    <input type="checkbox" id="switch" />

    <script>
        var switchWidget = $("#switch").kendoMobileSwitch();
    </script>

## Checking/Unchecking the Mobile Switch

The checked state of the mobile Switch depends on the [`checked` configuration option](/api/mobile/switch#checked)
or the `checked` attribute of the widget element.

### Initialize Kendo mobile Switch from checked `input`

    <input type="checkbox" id="switch" checked="checked" />

    <script>
        var switchWidget = $("#switch").kendoMobileSwitch();
    </script>

### Initialize checked mobile Switch using jQuery plugin syntax

    <input type="checkbox" id="switch" />

    <script>
        var switchWidget = $("#switch").kendoMobileSwitch({ checked: true });
    </script>

## Specifying the Text of the Labels

### Customize Kendo mobile Switch on/off labels

    <input type="checkbox" id="switch" />

    <script>
        var switchWidget = $("#switch").kendoMobileSwitch({ onLabel: "YES", offLabel: "NO" });
    </script>

