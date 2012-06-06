## Description


kendo.mobile.ui.ModalView.Description

The Kendo ModalView is used to present self-contained functionality in the context of the current task.  

### Getting Started

The Kendo mobile Application will automatically initialize a mobile ModalView widget for every `div` element with `role` data attribute set to `modalview` present in the views/layouts markup.
Alternatively, it can be initialized using jQuery plugin syntax. The ModalView element may contain optional header and/or footer. A mobile scroller is automatically initialized around the contents of the element.

#### ModalView with header and footer

    <div data-role="view">
     <a href="#foo" data-rel="modalview">Foo</a>
     <div data-role="modalview" id="foo">
       <div data-role="header">
           <div data-role="navbar">
               <a data-align="right" data-role="button">Close</a>
           </div>
       </div>
    
       <ul data-role="listview">
         <li>Foo</li>
       </ul>
    
       <div data-role="footer">
          <div data-role="navbar">
              <a data-align="right" data-role="button">Details</a>
          </div>
       </div>
     </div>
    </div>


### Opening a ModalView

The widget can be open when any mobile navigational widget (listview, button, tabstrip, etc.) is tapped.
To do so, the navigational widget should have `data-rel="modalview"` and `href` attribute pointing to the ModalView's element `id` set (prefixed with `#`, like an anchor).

#### Button, which opens a ModalView

    <div data-role="view">
     <a href="#foo" data-rel="modalview">Foo</a>
     <div data-role="modalview" id="foo">
      ...
     </div>
    </div>


#### Button, which closes a ModalView

    <div data-role="view">
     <a href="#foo" data-rel="modalview">Foo</a>
     <div data-role="modalview" id="foo">
       <div data-role="header">
           <div data-role="navbar">
               <a data-align="right" data-click="closeModalView" data-role="button">Close</a>
           </div>
       </div>
    
      Foo
     </div>
    </div>
    
    <script>
    function closeModalView(e) {
     // find the closest modal view, relative to the button element.
     var modalView = e.sender.element.closest("[data-role=modalview]").data("kendoMobileModalView");
     modalView.close();
    }
    </script>



------------------------------------------

## Configuration

### `height` : **Number**  

The height of the ModalView container in pixels. If not set, the element style is used.

### `modal` : **Boolean** *(default: true)* 

 When set to false, the ModalView will close when the user taps outside of its element.

### `width` : **Number**  

The width of the ModalView container in pixels. If not set, the element style is used.



------------------------------------------

## Methods

### `close`()


Close the ModalView
### `open`(target)


Open the ModalView
#### Parameters 

##### target `jQueryObject`

(optional) The target of the ModalView



------------------------------------------

## Events

### `open`
Fires when the ModalView is shown.

kendo.mobile.ui.ModalView#open



#### Example

    <div data-role="view">
     <a href="#foo" data-rel="modalview">Foo</a>
     <div data-role="modalview" id="foo" data-open="logTarget">
      Foo
     </div>
    </div>
    
    <script>
    function logTarget(e) {
      console.log(e.target); // <a href="#foo" ...
    }
    </script>

#### Event Data 

##### e.target `jQueryObject`

The invocation target of the ModalView.

