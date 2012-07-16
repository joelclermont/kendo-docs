---
title: kendo.mobile.ui.Scroller
slug: mobile-kendo.mobile.ui.scroller
tags: api,mobile
publish: true
---

# kendo.mobile.ui.Scroller

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
