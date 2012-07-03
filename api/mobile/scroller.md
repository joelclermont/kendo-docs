---
title: kendo.mobile.ui.Scroller
slug: mobile-kendo.mobile.ui.scroller
tags: api,mobile
publish: true
---

# kendo.mobile.ui.Scroller

## Description



The Kendo Mobile Scroller widget enables touch friendly kinetic scrolling for the contents of a given DOM element.  

### Getting Started

Each mobile View initializes a scroller for its content element. In addition to that, a scroller will be initialized for every element with a
`role` data attribute set to `scroller`.
Alternatively, it can be initialized using jQuery plugin syntax in the containing mobile View **init event handler**.


For the scroller to work, its element should have fixed dimensions (width and/or height) set.

#### Initialize mobile Scroller using a role data attribute.

    <div data-role="scroller">
      Foo
    </div>

#### Initialize mobile Scroller using jQuery plugin syntax

    <div id="scroller"></div>
    <script>
    var scroller = $("#scroller").kendoMobileScroller();
    </script>

#### Obtain the current mobile view scroller

    <div data-role="view" data-init="getScroller">
      Foo
    </div>
    <script>
     function getScroller(e) {
        var scroller = e.view.scroller;
     }
    </script>

The mobile Scroller widget exposes the following fields:

*   **scrollTop** - the number of pixels that are hidden from view above the scrollable area.
*   **scrollLeft** - the number of pixels that are hidden from view to the left of the scrollable area.

## Configuration

### elastic `Boolean`*(default: true)*

 Weather or not to allow out of bounds dragging and easing.

### pullOffset `Number`*(default: 140)*

 The threshold below which a releasing the scroller will trigger the pull event.
Has effect only when the pullToRefresh option is set to true.

### pullTemplate `String`*(default: Pull to refresh)*

 The message template displayed when the user pulls the scroller.
Has effect only when the pullToRefresh option is set to true.

### pullToRefresh `Boolean`*(default: false)*

 If set to true, the scroller will display a hint when the user pulls the container beyond its top limit.
If a pull beyond the specified pullOffset occurs, a pull event will be triggered.

### refreshTemplate `String`*(default: Refreshing)*

 The message template displayed during the refresh.
Has effect only when the pullToRefresh option is set to true.

### releaseTemplate `String`*(default: Release to refresh)*

 The message template displayed when the user pulls the scroller below the
pullOffset, indicating that pullToRefresh will occur.
Has effect only when the pullToRefresh option is set to true.

## Methods

### pullHandled

Indicate that the pull event is handled (i.e. data from the server has been retrieved).

#### Custom pull to refresh view scroll handling

     <div data-role="view" data-init="initPullToRefreshScroller">
         <h2 id="pull-to-refresh-clock"></h2>
     </div>
    <script>
    
     function updateClock() {
         pullTime = kendo.toString(new Date(), "hh:mm:ss tt" );
         $("#pull-to-refresh-clock").html("Last update at " + pullTime + ". <br /> Pull to refresh.");
     }
    
     function initPullToRefreshScroller(e) {
         var scroller = e.view.scroller;
    
         scroller.setOptions({
             pullToRefresh: true,
             pull: function() {
                 updateClock();
                 setTimeout(function() { scroller.pullHandled(); }, 400);
             }
         })
     }
    </script>

### reset

Scrolls the container to the top.

### scrollHeight

Returns the height in pixels of the scroller content.

### scrollTo

Scrolls the container to the specified location

#### Parameters

##### x `Number`

The horizontal offset in pixels to scroll to.

##### y `Number`

The vertical offset in pixels to scroll to.

### scrollWidth

Returns the width in pixels of the scroller content.

## Events

### pull

Fires when the pull option is set to true, and the user pulls the scrolling container beyond the specified pullThreshold.

### resize

Fires when the scroller dimensions change (e.g. orientation change or resize)

### scroll

Fires when the user scrolls through the content.

#### Bind to scroller scroll event in view init

    <div data-role="view" data-init="attachToScroller"> ... </div>
     <script>
        function attachToScroller(e) {
          var scroller = e.view.scroller;
          scroller.bind("scroll", function(e) {
             console.log(e.scrollTop);
             console.log(e.scrollLeft);
          });
        }
     </script>

#### Event Data

##### e.scrollTop `Number`

The number of pixels that are hidden from view above the scrollable area.

##### e.scrollLeft `Number`

The number of pixels that are hidden from view to the left of the scrollable area.