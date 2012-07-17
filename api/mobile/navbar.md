---
title: kendo.mobile.ui.NavBar
slug: mobile-kendo.mobile.ui.navbar
tags: api,mobile
publish: true
---

# kendo.mobile.ui.NavBar

## Methods

### title

Update the title element text. The title element is specified by setting the `role` data attribute to `view-title`.

#### Example

    <div data-role="navbar" id="foo">
        <span data-role="view-title"></span>
    </div>

    <script>
      $("#foo").data("kendoMobileNavBar").title("Foo");
    </script>

#### Parameters

##### value `String`

The text of title
