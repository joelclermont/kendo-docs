# kendo.mobile.ui.View

## Description



The Kendo mobile View widget represents a screen in the kendo mobile Application. The
Application automatically instantiates a mobile View for each element with a `role` data attribute set
to **view**.

#### Hello World mobile View

    <div data-role="view">Hello world!</div>

### Headers and Footers

By default, the mobile View contents stretch to fit the application element.
In addition to that, The mobile View may also have a header and a footer.
In order to mark header and footer elements, add block elements (`div`, `header`, `footer`, etc.) with attribute `data-role="header"` and
`data-role="footer"`. 

#### Mobile View with Header and Footer

    <div data-role="view">
      <div data-role="header">Header</div>
      Hello world!
      <div data-role="footer">Footer</div>
    </div>

**Important:**


Because of the OS UI design conventions, the header and the footer switch positions when an Android device is detected.
Usually the footer hosts a mobile Tabstrip widget, which is located at the bottom of the screen on iOS,
and at the top of the screen in Android applications.  

### View Parameters

Navigational widgets can pass additional URL parameters when navigating to Views. The parameters will be accessible in the  view `show` event handlers.

#### Button with additional URL parameters

    <a data-role="button" href="#foo?bar=baz">Link to FOO <strong>View</strong> with bar parameter set to baz</a>
    <div data-role="view" id="foo" data-show="fooShow">
    </div>
    
    <script>
    function fooShow(e) {
         e.view.params // {bar: "baz"}
    }
    </script>

### View DOM elements

Each mobile View instance exposes the following fields:

*   **header** - the view (or the applied mobile layout) header DOM element;
*   **footer** - the view (or the applied mobile layout) footer DOM element;
*   **content** - the view content DOM element;
*   **scrollerContent** - the view mobile scroller container DOM element. Recommended if the mobile View
 contents need to be manipulated or **replaced**.

## Configuration

### `model` : **String | ObservableObject** *(default: null)*

 The MVVM model to bind to. If a string is passed, The view
will try to resolve a reference to the view model variable in the global scope.

#### Example

    <script>
     var foo = { bar: "baz" }
    </script>
    
    <div data-role="view" data-model="foo">
       <span data-bind="text:bar"></span>
    </div>

### `stretch` : **Boolean** *(default: false)*

 If set to true, the view will stretch its child contents to occupy the entire view, while disabling kinetic scrolling.
Useful if the view contains an image or a map.

### `title` : **String** 

 The text to display in the navbar title (if present) and the browser title.

## Methods

## Events

### beforeShow

Fires before the mobile View becomes visible. The event can be prevented by calling the `preventDefault` method of the event parameter, in case a redirection should happen.

#### Event Data

##### e.view `jQuery`

The mobile view instance

### hide

Fires when the mobile View becomes hidden.

#### Event Data

##### e.view `jQuery`

The mobile view instance

### init

Fires after the mobile View and its child widgets are initialized.

#### Event Data

##### e.view `jQuery`

The mobile view instance

### show

Fires when the mobile View becomes visible.

#### Event Data

##### e.view `jQuery`

The mobile view instance