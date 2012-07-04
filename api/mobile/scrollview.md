---
title: kendo.mobile.ui.ScrollView
slug: mobile-kendo.mobile.ui.scrollview
tags: api,mobile
publish: true
---

# kendo.mobile.ui.ScrollView

## Description



The Kendo Mobile ScrollView widget is used to scroll content wider than the device screen.

### Getting Started

<p>The Kendo Mobile Application automatically initializes the Mobile ScrollView for every element with `role` data attribute set to `scrollview` present in the views' markup.
Alternatively, it can be initialized using jQuery plugin syntax in the containing mobile View **init event handler**.

#### Initialize mobile ScrollView using a role data attribute.

    <div data-role="scrollview">
      Foo
    </div>

#### Initialize mobile ScrollView using jQuery plugin syntax.

    <div data-role="view" data-init="initScrollView">
      <div id="scrollView">
        <div data-role="page">Foo</div>
        <div data-role="page">Bar</div>
      </div>
    </div>
    <script>
    function initScrollView(e) {
      e.view.element.find("#scrollView").kendoMobileScrollView();
    }
    </script>

### Pages

Content pages may be defined in order to display exactly one item per page. Pages are automatically resized
when the device is rotated. To define a page, wrap the content in a div with `data-role="page"` attribute set.

#### ScrollView with pages

    <div data-role="scrollView">
       <div data-role="page">Foo</div>
       <div data-role="page">Bar</div>
    </div>

## Configuration

### bounceVelocityThreshold `Number`*(default: 1.6)*

 The velocity threshold after which a swipe will result in a bounce effect.

### duration `Number`*(default: 300)*

 The milliseconds that take the ScrollView to snap to the current page after released.

### page `Number`*(default: 0)*

 The initial page to display.

### velocityThreshold `Number`*(default: 0.8)*

 The velocity threshold after which a swipe will navigate to the next page (as opposed to snapping back to the current page).

## Methods

### content

Update the scrollview HTML content

#### Example

    <div data-role="scrollview" id="scrollview"></div>
    
    <script>
       $("#scrollview").data("kendoMobileScrollView").content("<span>Foo</span>");
    </script>

#### Parameters

##### content `String | jQuery`

the new scrollView content.

### refresh

Redraw the mobile ScrollView pager. Called automatically on device orientation change event.

#### Example

    <div data-role="scrollview" id="scrollview"></div>
    
    <script>
       $("#scrollview").data("kendoMobileScrollView").refresh();
    </script>

### scrollTo

Scroll to the given page. Pages are zero-based indexed.

#### Example

    <div data-role="scrollview" id="scrollview"></div>
    
    <script>
       // Scroll to the second page of the scrollView
       $("#scrollview").data("kendoMobileScrollView").scrollTo(1);
    </script>

#### Parameters

##### page `Number`

The page to scroll to.

## Events

### change

Fires when the widget page is changed.

#### Event Data

##### e.page `jQuery`

The current page (zero based index)