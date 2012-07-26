---
title: kendo.mobile.ui.ModalView
slug: mobile-kendo.mobile.ui.modalview
tags: api,mobile
publish: true
---

# kendo.mobile.ui.ModalView

## Configuration

### height `Number`

The height of the ModalView container in pixels. If not set, the element style is used.

### modal `Boolean`*(default: true)*

 When set to false, the ModalView will close when the user taps outside of its element.

### width `Number`

The width of the ModalView container in pixels. If not set, the element style is used.

## Methods

### close

Close the ModalView

### open

Open the ModalView

#### Parameters

##### target `jQuery`

(optional) The target of the ModalView

## Events

### open

Fires when the ModalView is shown.

#### Example

    <div data-role="view">
        <a data-role="button" href="#foo" data-rel="modalview">Foo</a>
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

##### e.target `jQuery`

The invocation target of the ModalView.
