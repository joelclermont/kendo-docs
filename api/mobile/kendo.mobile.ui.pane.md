## Description


kendo.mobile.ui.Pane.Description

### Mobile Pane

The mobile Pane widget groups one or more **mobile views** within the main view application. The mobile
SplitView widget allows a side by-side display of several panes. The mobile PopOver automatically instantiates a mobile Pane widget for its
contents.

The mobile Pane widget acts like an embedded mobile application, with most of the application
features available: support for local/remote views, default layout and transition, lading, etc. with one
exception being the browser history support. Navigating within the pane will not update the history state, so
deep linking to a pane state is not supported.

### Navigating across panes

By default, navigational widgets will change views in the containing pane. To target another pane, use
`target` data attribute set to the **id** of the pane. To change views in the mobile
application, use `data-target="_top"`.

#### Navigating across panes

    <div data-role="splitview" id="main">
       <div data-role="pane" id="side-pane">
         <div data-role="view">
            <a data-role="button" href="#bar" data-target="main-pane">Bar (main pane)</a>
            <a data-role="button" href="#baz" data-target="_top">Baz (application)</a>
         </div>
       </div>
    
       <div data-role="pane" id="main-pane">
         <div data-role="view" id="foo">
            Foo
         </div>
         <div data-role="view" id="bar">
            Bar
         </div>
       </div>
     </div>
    
     <div data-role="view" id="baz">
        <a data-role="button" href="#main">Go back to splitview</a>
     </div>



------------------------------------------

## Configuration

### `initial` : **String**  

 The id of the initial mobilie View to display.

### `layout` : **String**  

 The id of the default Pane Layout.

### `loading` : **String** *(default: Loading...)* 

 The text displayed in the loading popup. Setting this value to false will disable the loading popup.

### `transition` : **String**  

 The default View transition.



------------------------------------------

## Methods

### `hideLoading`()


Hide the loading animation.
### `navigate`(url, transition)


Navigate the local or remote view.

#### Navigate to a remote view

    <div data-role="pane" id="main-pane">
    </div>
    
    <script>
    var pane = $("#main-pane").data("kendoMobilePane");
    pane.navigate("settings.html");
    </script>


#### Navigate to a local view

    <div data-role="pane" id="main-pane">
      <div data-role="view" id="foo"> ... </div>
    </div>
    
    <script>
    var pane = $("#main-pane").data("kendoMobilePane");
    pane.navigate("#foo");
    </script>

#### Parameters 

##### url `String`

The id or url of the view.

##### transition `String`

The transition to apply when navigating. See View Transitions section for more
information.

### `showLoading`()


Show the loading animation.
### `view`()`View`


Get a reference to the current view.
#### Returns 

`View` the view instance.



------------------------------------------

## Events

### `navigate`
Fires when pane navigates to a view.

kendo.mobile.ui.Pane#navigate


#### Event Data 

##### e.url `jQueryObject`

The url of the view

### `viewShow`
Fires after the pane displays a view.

kendo.mobile.ui.Pane#viewShow


#### Event Data 

##### e.view `View`

The displayed view

