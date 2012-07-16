---
title: Mobile ModalView Overview
slug: getting-started.mobile.modalview
tags: getting-started,mobile
publish: true
---

# Mobile ModalView Overview

The Kendo ModalView is used to present self-contained functionality in the context of the current task.

## Getting Started

The Kendo mobile Application will automatically initialize a mobile ModalView widget for every `div` element with `role` data attribute set to `modalview` present in the views/layouts markup.
Alternatively, it can be initialized using jQuery plugin syntax. The ModalView element may contain optional header and/or footer. A mobile scroller is automatically initialized around the contents of the element.

> **Important:** The ModalView should be defined in the View where it will be invoked. When used in conjunction with a SplitView, the ModalView should be placed
as a child of a View inside it or if you want it to cover the whole SplitView - as a direct child of it.

### ModalView with header and footer

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

## Opening a ModalView

The widget can be open when any mobile navigational widget (listview, button, tabstrip, etc.) is tapped.
To do so, the navigational widget should have `data-rel="modalview"` and `href` attribute pointing to the ModalView's element `id` set (prefixed with `#`, like an anchor).

### Button, which opens a ModalView

    <div data-role="view">
        <a href="#foo" data-rel="modalview">Foo</a>

        <div data-role="modalview" id="foo">
            ...
        </div>
    </div>

### Button, which closes a ModalView

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

