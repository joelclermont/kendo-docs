---
title: kendo.mobile.ui.ScrollView
slug: mobile-kendo.mobile.ui.scrollview
tags: api,mobile
publish: true
---

# kendo.mobile.ui.ScrollView

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
