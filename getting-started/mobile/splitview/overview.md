---
title: Mobile SplitView overview
slug: gs-mobile-splitview
tags: getting-started,mobile
publish: true
---

# Mobile SplitView Overview

The mobile SplitView is a tablet-specific view that consists of two or more **mobile Pane widgets**. The
Mobile Application automatically instantiates a mobile SplitView for each element with a `role` data attribute set
to **splitview**.

**Important:** unlike most widgets, the splitview element **should not be nested**
in a view, but should be put as an immediate child of the mobile application element.

## Mobile SplitView with two panes

    <div data-role="splitview">

      <div data-role="pane" id="side-pane">
          <div data-role="view" data-title="Messages">
             <ul data-role="listview">
               <li><a href="#foo" data-target="main-pane">Foo</a></li><!-- link to main pane -->
               <li><a href="#bar">Bar</a></li><!-- link to same pane -->
             </ul>
          </div>
      </div>

      <div data-role="pane" data-layout="main-default" id="main-pane">
          <div data-role="view" data-title="Messages">
              No message selected
          </div>

          ...

          <div data-role="layout" data-id="main-default">
              <div data-role="header">
                  <div data-role="navbar">
                      <span data-role="view-title"></span>
                  </div>
              </div>
          </div>
      </div>

    </div>

# Customizing appearance

By default Kendo UI Mobile is configured to show a horizontal SplitView with smaller left and bigger right pane in 1:2 proportion.
In order to resize one of the panes, use CSS to set its width or adjust the flexibility of the flex boxes (if the width is set, the other pane flexibility should be set to a high numer, like 1000).

## Set pane width to 300px or change the proportions to 1:3

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

    <style>
        #side-pane { width: 300px; }
        #main-pane { -webkit-box-flex: 1000; }
    </style>
    or
    <style>
        #main-pane { -webkit-box-flex: 3; }
    </style>

Additionally you can split your view to more panes by adding them directly. You can also make them stack vertically
by setting data-style="vertical" on your SplitView.

## Make SplitView to stack vertically.

    <div data-role="splitview" id="main" data-style="vertical">
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

